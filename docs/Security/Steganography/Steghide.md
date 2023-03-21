
#### Installation 

```
sudo apt-get install steghide
```


#### Encryption 


```
steghide embed –ef [file.txt] –cf [img]
```

#### Exemple : hide message data.txt in image.jpg

```
steghide embed –ef data.txt –cf image.jpg
```


#### Extraction 

```
steghide extract -sf img.jpg
```
