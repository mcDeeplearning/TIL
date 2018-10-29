# telegram bot

### install

- telegram 설치

### bot init

- @BotFather  검색
- start 버튼클릭
- /newbot 입력
- 이름을 생성 => 중복가능
- username => `bot`으로 끝나야하고 유니크한 값
- `token`, `url` 
- url 클릭하여 봇 활성화

### telegram.py

```python
import requests
token = "봇의 토큰값"
method_name = "getUpdates"
url = 'https://api.telegram.org/bot{0}/{1}'.format(token,method_name)

print(url)
print(requests.get(url))
```

