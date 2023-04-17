
#### Scraping template

```python
from bs4 import BeautifulSoup, NavigableString, Tag
from urllib.request import Request, urlopen

url = "[URL]"

req = Request(url, headers={'User-Agent': 'Mozilla/5.0'})
webpage = urlopen(req).read()

soup = BeautifulSoup(webpage, 'html.parser')
```


---


#### Get text value

1. Find **div** where class is **div_class**

	```python
	val = soup.find('div', attrs={'class': 'div_class'})
	```

2. Get associated text

	```python
	val.getText()
	```