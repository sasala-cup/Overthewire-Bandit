## Task

```
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
```

## Tools

ssh, [[nc]], cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …)

## Approach

1. Create a listening netcat-server on a custom port and let it respond with the password
	cat password.txt | nc -l -p 1234
2. Connect to the port via sconnect
	./sconnec 1234

## Password

bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY