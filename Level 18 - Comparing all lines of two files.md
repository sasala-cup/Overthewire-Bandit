## Task

There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

## Tools

cat, grep, ls, diff

## Approach

1. Log in with the ssh-key from [[Level 17 - Scanning and filtering ports]]
	ssh -i sshkeyLvl17.private bandit17@bandit.labs.overthewire.org -p 2220
2. Compare both files line by line for differences (-u)
	diff -u passwords.old passwords.new
3. Notice the differing lines
	==-==RL3QgeKo8FFveuQpIwkGsxCVTfqxXYes
	==+==OQxXZjELndr90zuhOTDYBEomI0SZITXI


## Password

OQxXZjELndr90zuhOTDYBEomI0SZITXI
