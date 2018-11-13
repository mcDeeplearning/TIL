# flask intro

- 파이썬 환경 설정
- 플라스크
  - `pip install flask`

- `app.py`

  ```python
  from flask import Flask
  app = Flask(__name__)
  
  # 요청이 들어오는 주소 설정
  @app.route("/")
  def hello():
      return "Hello World!"
  ```

- 서버 실행

  - `flask run --host 0.0.0.0 --port 8080`
  - 

