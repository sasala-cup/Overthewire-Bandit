## Task

```
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: Looking at shell scripts written by other people is a very useful skill. The script for this level is intentionally made easy to read. If you are having problems understanding what it does, try executing it to see the debug information it prints.
```

## Tools

cron, crontab, crontab(5) (use “man 5 crontab” to access this)


## Approach

1. Look into the directory mentioned in the task
	ls /etc/cron.d
	=> cronjob_bandit23
2. Look into the file
	cat cronjob_bandit23
	=> usr/bin/cronjob_bandit23.sh
3. Look into the given script
	=> echo I am user $myname | md5sum | cut -d ' ' -f 1
	=>cat /etc/bandit_pass/myname > /tmp/mytarget
4. Substitute $myname with bandit23 and encode with md5 (!when with a encoder make sure to add a new line aswell)
	=>8ca319486bfbbc3663ea0fbe81326349
5. Look into the file
	cat /tmp/8ca319486bfbbc3663ea0fbe81326349
	=>8ca319486bfbbc3663ea0fbe81326349


## Password

gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw