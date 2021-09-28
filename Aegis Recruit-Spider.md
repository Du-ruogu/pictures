```python
import requests
from bs4 import BeautifulSoup

r = requests.get('https://www.hao123.com/')
r.encoding = 'utf-8'
demo = r.text
soup = BeautifulSoup(demo, "html.parser")
es = soup.find_all(id = 'coolsites_wrapper')
es1 = [str(i) for i in es]
es2 = ' '.join(es1)
soup1 = BeautifulSoup(es2, 'html.parser')
for link in soup1.find_all('a', 'sitelink icon-site'):
    print(link.get('href') +' ' + link.get('data-title'))
```
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E5%9B%BE%E7%89%8720210928091448.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E5%9B%BE%E7%89%8720210928091517.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E5%9B%BE%E7%89%8720210928091536.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E5%9B%BE%E7%89%8720210928091635.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E5%9B%BE%E7%89%8720210928091722.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E6%88%AA%E5%9B%BE20210928091819.png)
![Alt text](https://github.com/Du-ruogu/pictures/blob/main/QQ%E6%88%AA%E5%9B%BE20210928092225.png)
