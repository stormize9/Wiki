#### Usage

1. To embed the message hidden.txt into the monkey.jpg image:


	```
	outguess -k "my secret pass phrase" -d hidden.txt monkey.jpg out.jpg
	```

 2. To extract hidden message from out.jpg


	```
	outguess -k "my secret pass phrase" -r out.jpg message.txt
	```



3. Embed a second message, use:


	```
	outguess -k "secret1" -d hide1.txt -E -K "secret2" -D hide2.txt monkey.jpg out.jpg
	```


4. Outguess  will  first  embed  hide1.txt  and  then hide2.txt  on  top  of it, using error correcting codes.  
5. The second message hide2.txt can be retrieved with


	```
	outguess -k "secret2" -e -r out.jpg message.txt
	```
