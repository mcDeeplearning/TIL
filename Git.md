# Git

> Git => 분산버전관리시스템

1. init
   1. 저장소를 만든다
2. add
   1. 임시저장 한다
   2. `git add .` 을 사용해서 현재 폴더 및 하위 모든 항목을 추가
   3. `git add text.txt`를 사용해서 원하는 파일 하나만 추가
3. commit
   1. 새로운 버전을 만든다
   2. `git commit -m "뭐가 수정됬나요"`
   3. `git log` => 커밋 이력을 확인해봅시다.
4. remote
   1. 원격 저장소 설정
   2. `git remote add origin _주_소_`
      1. origin이 아니여도 상관 없지만 통상적으로 origin사용
5. push
   1. 내가 원하는 원격 저장소에 코드를 올리겠다
   2. `git push origin master`
6. 자주사용하는 명령어
   1. git status
      1. 폴더/파일의 변화 감지
   2. git diff
      1. 몇번째 줄이 어떻게 바꼈는지
   3. git log
      1. 커밋 이력 확인
   4. git remote

- [git 입문](https://backlog.com/git-tutorial/kr/)

- [git scm](https://git-scm.com/docs)