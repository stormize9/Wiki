
#### Template python

```python
from urllib.request import Request, urlopen
import json 
import requests
import re
import sqlite3
import sys
from bs4 import BeautifulSoup

url = "[URL]"


####OPTIONNEL
payload = {}
headers = {
      'Content-Type': 'application/json',
      'Authorization': 'Token [TOKEN]'
    } 

response = requests.request("GET", url, verify=False)
json_data = response.json()


print(json_data)
```