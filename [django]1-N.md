# 1:N 댓글

### 0. 프로젝트 생성

> 파이썬 가상환경 설정도 프로젝트 이름과 동일하게 해주세요

- 프로젝트 이름 : either
- 앱 이름 : question

### 1. 모델 설정

- question 모델
  - CharField로 설정할때 max_length를 넣어야합니다
  - title : string
  - answerA : string
  - answerB : string
- 마이그레이션
- 어드민 페이지에 추가
- superuser 생성





+++



### Question

- Create - 완료
- Read - 완료
- Update - 완료
- Delete

### Comment

- Create - 완료
- Read - 완료
- Delete

#### +추가

- 각각의 기능들로 가는 링크들 생성 
  - 예) 수정하기 버튼, 글보기 버튼
  - {% url %} => 얘를 사용해서 링크 만들기



























