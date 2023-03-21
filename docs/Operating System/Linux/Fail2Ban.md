
#### See Fail2Ban status

```bash
sudo fail2ban-client status sshd
```


#### See ban IPs

```bash
sudo zgrep 'Ban' /var/log/fail2ban.log*
```


#### Ban IP manually

1. Get jail name : 

	```bash
	sudo fail2ban-client status
	```

2. Ban IP W.XX.YY.ZZ

	```bash
	sudo fail2ban-client -vvv set JAIL banip WW.XX.YY.ZZ
	```

3. Check IP is banned
	```bash
	sudo fail2ban-client status sshd
	```


#### Unban IP manually


```
sudo fail2ban-client -vvv set JAIL unbanip WW.XX.YY.ZZ
```

