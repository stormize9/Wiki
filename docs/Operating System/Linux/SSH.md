
### Permissions

#### Authorize root login 

1. Open sshd_config


	```shell
	sudo nano /etc/ssh/sshd_config
	```



2. Modify these lines


	```shell
	# Authentication:
	#LoginGraceTime 2m
	PermitRootLogin yes
	#StrictModes yes
	#MaxAuthTries 6
	#MaxSessions 10
	```



3. Restart the server


	```shell
	sudo systemctl restart sshd
	```




---

### Clés SSH


1. Générer clé


	```shell
	ssh-keygen
	```


2. Copier clé sur serveur distant

	```shell
	ssh-copy-id [user]@[ip]
	```

3. Tester connexion sans mot de passe

	```shell
	ssh [user]@[ip]
	```


- - - 
#### Specify a ssh key


```
	ssh -i <key> <user>@<ip>
```



---

### Log SSH

See all logs 

```
sudo grep 'sshd' /var/log/auth.log
```

Show login attempts 

```
sudo lastb -F
```

Show failed password attempts 
```
sudo grep 'Failed password' /var/log/auth.log
```


Show success password attempts  


```
sudo grep 'Accepted password' /var/log/auth.log
```
