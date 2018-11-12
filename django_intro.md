# django intro

### 0. [파이썬 환경설정](https://github.com/mcDeeplearning/TIL/blob/master/파이썬%20환경설정.md)



### 1. django 설정

- 장고 설치
  - 전역에서 django-admin 이라는 명령어를 사용하기 위해서
  - `pip install django`
- django 프로젝트 생성
  - `django-admin startproject <프로젝트이름>`
  - `cd <프로젝트이름>`
- 로컬 파이썬 버전 셋팅
  - `pyenv virtualenv 3.6.1 <프로젝트이름>`
  - `pyenv local <프로젝트이름>`
  - `pip install django`
- django 앱 생성
  - `django-admin startapp <앱이름>`
- django server 실행
  - `python manage.py runserver $IP:$PORT`













