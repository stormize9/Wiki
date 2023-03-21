
<div><p align="center">
<img src="https://1000logos.net/wp-content/uploads/2017/03/LINUX-LOGO.png"  alt=”logo” width=72 height=72>
<p align="center">Linux® is an open source operating system (OS). An operating system is the software that directly manages a system’s hardware and resources, like CPU, memory, and storage. The OS sits between applications and hardware and makes the connections between all of your software and the physical resources that do the work.</p></div>

#### Table of content

> [Crontab](/Operating%20System/Linux/Crontab)

> [Fail2Ban](/Operating%20System/Linux/Fail2Ban)

> [Grep](/Operating%20System/Linux/Grep)

> [Journalctl](/Operating%20System/Linux/Journaltcl)

> [Open ports](/Operating%20System/Linux/Open%20ports)

> [SSH](/Operating%20System/Linux/SSH)

> [Backup](/Operating%20System/Linux/Backup)



<br>
<br>


#### Change timezone in a docker container

1. Log into bash of your container:

	```shell
	docker exec -u 0 -it mycontainer bash
	```

2. Remove the symbolic link file (/etc/localtime):

	```shell
	sudo rm -rf /etc/localtime
	```

3. Identify the timezone you want to configure and create the symbolic link for it: 
	For Paris


	```shell
	ln -s /usr/share/zoneinfo/Europe/Paris /etc/localtime
	```

4. Verify

	```shell
	date
	```