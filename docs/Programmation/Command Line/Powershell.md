
#### SCP


1. Linux → Windows

	```powershell
	scp -r [id]@[ip]:/home/ ./
	```

2. Windows -> Linux

	```powershell
	scp -r .\[file] [id]@[ip]:/home/
	```

3. Specify a port


	```powershell
	scp -P 5789 -r [id]@[ip]:/home/ ./
	```


---

#### Generation tree folder

```powershell
$Path = "C:\folder"
Tree $Path /F | Select-Object -Skip 2 | Set-Content C:\folder\output.txt
```

- - - 
#### Commands about domain and administrators

 
Displays all information in the current access token, including the current user name, security identifiers (SID), privileges, and groups that the current user belongs to.

```powershell
whoami /all
```
<br>

This command lists the users of the domain administrator group.

```Powershell
Net group “domain admins” /domain
```
<br>

This command lists all administrator users of the local PC.

```Powershell
Net localgroup administrators
```
<br>

This command returns a list of all trusted domains.


```Powershell
Nltest /domain_trusts /all_trusts
```
