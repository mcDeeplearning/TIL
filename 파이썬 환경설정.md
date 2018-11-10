# 파이썬 환경설정

### [pyenv](https://github.com/pyenv/pyenv)

- install
```bash
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```

- 환경변수 설정
```bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bashrc

source ~/.bashrc
# 환경변수 추가후 bashrc 실행 => 터미널 새로고침
# exec $SHELL => 이명령어를 실행해도 됨!!
```

- python install
```bash
pyenv install 3.6.1 # pyenv를 통해서 python 3.6.1을 설치
pyenv global 3.6.1  # 전역으로 버전 설정
python -V # 파이썬 버전 확인
pyenv versions # 사용가능한 파이썬 버전 리스트 출력
```

### [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv)

- install
```bash
git clone https://github.com/pyenv/pyenv-virtualenv.git $(pyenv root)/plugins/pyenv-virtualenv
```

- 환경변수 설정
```bash
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bashrc
source ~/.bashrc
```

- 가상환경 만들기
```bash
pyenv virtualenv <파이썬 버전> <설정할 가상환경 이름>
pyenv versions # 사용가능한 버전 확인
```

- 가상환경 사용하기
```bash
# 가상환경 활성화
pyenv activate tele
# 아래명령어도 사용가능하지만 deactivate 불가
# pyenv shell tele 

#(tele) ochange:~/workspace $ 
# 커맨드라인 앞에 가상환경 이름이 나와야 합니다.mc

# 가상환경 비활성화
pyenv deactivate

# 가상환경 삭제
pyenv uninstall <가상환경이름>

# 위의 명령어는 전역에서 사용하기 위한 명령어
# 폴더별로 환경을 다르게 사용하기 위해 local로 설정!!
```