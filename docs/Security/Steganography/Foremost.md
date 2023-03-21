
Foremost is **a program that recovers files based on their headers , footers and internal data structures**. It can be useful when dealing with png images. It can be installed with apt however the source can be found on github. Useful commands: foremost -i file : extracts data from the given file.

#### Usage 

1. Help


	```shell
	foremost -h
	```

2. Extract files of type 'gif and pdf' from the file 'img.jpg'

	```shell
	foremost -t gif,pdf -i img.jpg
	```
