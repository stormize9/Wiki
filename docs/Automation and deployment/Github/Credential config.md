
#### Setting Git username for every repo

1. Set username
	```shell
	git config --global user.name "Mona Lisa"
	```

2. Confirm that you have set the Git username correctly:

	```shell
	git config --global user.name
	```


#### Setting Git username for one repository


1. Go inside the work project

	```shell
	cd /path/to/work/directory
	```


2. Set username
	```shell
	git config user.name "Mona Lisa"
	```

3. Confirm that you have set the Git username correctly:

	```shell
	git config user.name
	```




#### Store password and id

1. Before a clone or a pull, do this command to store credentials

	```shell
	git config --global credential.helper store
	```
