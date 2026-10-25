## Task

```
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.
```

## Tools

cron, crontab, crontab(5) (use “man 5 crontab” to access this)

## Approach

1. Look into the cron directory
	ls /etc/cron.d
2. Look into the relevant cronjob (cronjob_bandit22)
	cat /etc/cron.d/cronjob_bandit22
		#!/bin/bash
		chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
		cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
3. Look into the mentioned folder
	/tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
		RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz

## Password

RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz