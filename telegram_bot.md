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

```python
import requests
token = "763337042:AAEjq0JPofKKdu9_oYwVdi5O5L8JGz_xl6E"
method_name = "getUpdates"
url = 'https://api.telegram.org/bot{0}/{1}'.format(token,method_name)

user_id = '602595803'
method_name = "sendmessage"
msg = "안녕하세요!!!"
msg_url = 'https://api.telegram.org/bot{0}/{1}?chat_id={2}&text={3}'.format(token,method_name,user_id,msg)
print(msg_url)
print(requests.get(msg_url))
```

