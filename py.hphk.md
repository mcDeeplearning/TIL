# day1

파이썬 기초 + 웹 입문

zzu.li/deep

### py.hphk.io

- 카카오톡 플러스친구 (@python) 친구추가

```python
# 안녕
print("안녕하세요")
```

```python
# 메뉴
import random
list = ["20층", "김밥카페", "양자강"]
pick = random.choice(list)

print("오늘의 추천 메뉴는 {menu}".format(menu=pick))
```

```python
# 로또
import random

list = list(range(1,46))
lucky = random.sample(list,6)

print("행운의 번호 : {}".format(sorted(lucky)))
```

```python
# 메뉴사진
import random
list = ["짜장면", "김밥", "탕수육"]
dict = {
  "짜장면":"url",
  "김밥":"url",
  "탕수육":"url"
}
pick = random.choice(list)

print("오늘의 메뉴는 {}입니다!!!".format(pick))
print(dict[pick])
```

```python
# 미세먼지
import requests
from bs4 import BeautifulSoup
url = 'http://openapi.airkorea.or.kr/openapi/services/rest/ArpltnInforInqireSvc/getCtprvnRltmMesureDnsty?serviceKey=QaGapZXPV5DTM72fy6lrf3hJnrJxhila1UVkPlUCo0N0g0F0RZ9WEngT8RkNjNo4IF%2BikV%2BthQLze39nK4IQjA%3D%3D&numOfRows=10&pageSize=10&pageNo=3&startPage=3&sidoName=%EC%84%9C%EC%9A%B8&ver=1.3'
request = requests.get(url).text
soup = BeautifulSoup(request,'xml')
gangnam = soup('item')[7]
location = gangnam.stationName.text
time = gangnam.dataTime.text
dust = int(gangnam.pm10Value.text)

print("{0} 기준 {1}의 미세먼지 농도는 {2}입니다.".format(time,location,dust))

if(dust > 150):
  print("매우나쁨")
elif(80 < dust <=150):
  print("나쁨")
elif(30< dust and dust <= 80 ):
  print("보통")
else:
  print("좋음")
```

```python
# 코스피
import requests
from bs4 import BeautifulSoup
url = "https://finance.naver.com/sise/"

html = requests.get(url).text
soup = BeautifulSoup(html, 'html.parser')
select = soup.select_one('#KOSPI_now')

print(select.text)
```



