## Task

The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

## Tools

ssh, ls, cat

## Approach

1. Connect to the level via ssh
	Get kicked out :(
2. Connect to ssh again but including ls in the ssh command
	ssh bandit18@bandit.labs.overthewire.org -p 2220 ls
	=> readme
3. Connect to ssh including cat readme to read the readme file
	ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
	=> KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI

## Password

KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI