
#### CLI Commands

Delete a folder/file in Windows 


```
rmdir /s folder\file_to_delete
```



#### Create X folder 

1. Create 200 folder 1,2…200

```
for /L %i in (1,1,200) do md %i
```


#### Move a lot of file in different folder


```
for /L %i in (1,1,200) do move %i.jpg %i/
```


#### Move all the subfile in the root folder


```
for /d %i in (*) do move %i\* .
```
