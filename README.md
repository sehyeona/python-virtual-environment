# python virtual environment
## method1. python built in
파이썬에서 제공하는 가상환경 설치 모드로서 사용하고 있는 파이썬과 같은 버전의 가상환경 폴더가 설치된다

### 1) 가상환경 생성
```
python3 -m venv {venv directory path}
```
### 2) 가상환경 실행
```
source {venv directory path}/bin/activate
```
### 3) 가상환경 종료
```
source deactivate
```

## method2. PYENV로 파이썬 버전 관리하기
### 1) pyenv 설치
```
brew update 
brew install pyenv
```
### 2) pyenv 로 사용할 수 있는 파이썬 버전 확인하기
```
$ pyenv install -list
```
#### output
평범한 파이썬부터 아나콘다, 미니콘다 등등 다양한 파이썬 배포판을 다운받을 수 있다.
```
Available versions:
  2.1.3
  2.2.3
  2.3.7
...
  anaconda-1.4.0
  anaconda-1.5.0
  anaconda-1.5.1
...
  miniconda-latest
  miniconda-2.2.2
...
```
### 3) python 설치
* 임의로 3.7.6 버전을 받아보자
```
pyenv install 3.7.5
```
* pyenv versions 명령어를 통해 지금까지 설치한 버전들 확인가능
```
pyenv versions 
* system (set by /Users/an/.pyenv/version)
  3.7.6
  3.8.2
```
* 다운받은 파이썬은 아래와 같은 폴더에 저장되어 있다.
```
/Users/{username}/.pyenv/versions 
```
OR 
```
~/.pyenv/versions
```
* 실행기를 이용하여 버전에 맞는 파이썬을 실행할 수 있음 
```
~/.pyenv/versions/{versionname}/bin/python
```
### 4) Virtualenv 설치
```
# Python2의 경우
pip install virtualenv virtualenvwrapper

# Python3의 경우
pip3 install virtualenv virtualenvwrapper
```
### 5) virtualenv를 이용하여 가상환경 설치
```
virtualenv --python={python version} {virtual environment name}
```
예를 들어 위에서 설치한 파이썬 3.7.6 버전에 대한 가상환경을 workspace폴더의 crawling폴더안에 venv로 만들어 주고 싶다면
```
virtualenv --python=~/.pyenv/versions/3.7.6/bin/python3 ~/workspace/crawling/venv
```










