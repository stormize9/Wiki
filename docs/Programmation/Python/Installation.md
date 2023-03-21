

#### Installation Python 3.9 Linux Debian

1. Check version of Python

	```shell
	python --version
	```

2. Update repo

	```shell
	sudo apt update
	```

3. Install Supporting Software

	```shell
	sudo apt install software-properties-common
	```

4. Add Deadsnakes PPA

	```shell
	sudo add-apt-repository ppa:deadsnakes/ppa
	sudo apt update
	```


5. Install Python 3.9

	```shell
	sudo apt install python3.9
	```

6. Check Python version


	```shell
	python3 --version
	```


---


#### PIP Installation Linux Debian

1.  Update system

	Run the command below:

	```shell
	sudo apt-get update
	```

2. Install pip3

	If Python 3 has already been installed on the system, execute the command below to install pip3:

	```shell
	sudo apt-get -y install python3-pip
	```

3. Verification

	To verify the installation, run the following command to cross check the version number:

	```shell
	pip3 --version
	```