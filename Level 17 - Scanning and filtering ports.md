## Task

The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Tools

ssh, telnet, [[nc]], ncat, socat, [[openssl]], s_client, nmap, netstat, ss

## Approach

1. Scan for listening ports using netcat
	nc -zv 10.0.1.36 31000-32000
2. Filter output for succeeded
	nc -zv 10.0.1.36 31000-32000 2>&1 | grep "succeeded"
		Connection to 10.0.1.36 31046 port [tcp/*] succeeded!
		Connection to 10.0.1.36 31518 port [tcp/*] succeeded!
		Connection to 10.0.1.36 31691 port [tcp/*] succeeded!
		Connection to 10.0.1.36 31790 port [tcp/*] succeeded!
		Connection to 10.0.1.36 31960 port [tcp/*] succeeded!

3. Check ports for ssl/tls connectivity and feed password (same as in [[Level 16]])
	openssl s_client -connect 10.0.1.36:port -ign_eof
		Successfull connection with output on port 31790 with the output of an ssh-key
4. Copy ssh-key onto your device