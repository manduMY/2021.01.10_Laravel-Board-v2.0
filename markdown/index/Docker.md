Docker - 초기 셋팅
---

# Window10에 도커 설치하기

<br/>

## 1. Docker를 사용하기 위해 가상화 기술인 Hyper-V 활성화
- 제어판 > 프로그램 설치 및 제거 > Window 기능 켜기/끄기 클릭 > Hyper-V 체크 확인 후 리부팅

<br/>
<br/>

## 2. Docker 설치파일 다운로드 및 설치
- 설치하는 방법은 쉬우니 Pass
- 설치 완료 후 재부팅한다
- git bash나 cmd를 열고 'docker version'을 쳐서 설치가 완료되었는지 확인한다

<br/>
<br/>

## 3. Image와 Container 생성
- docker pull ubuntu:latest 입력한다 (docker 안에 ubuntu image 생성)
- docker run -it -p 80:80 --name laravel ubuntu bash 입력한다 (container port 80, host port 80으로 포트포워딩 하고 laravel container 생성)
- 만약에 백그라운드에서 동작하게끔 하고 싶다면 위 명령어에서 옵션에 -d를 추가하면 된다.
<br/>
### 컨테이너 실행법
- docker ps를 입력해서 현재 컨테이너가 동작중인지 확인한다.
- 컨테이너가 동작하고 있지 않다면 docker에 로그인 후 해당 container를 동작시킨다.
- docker exec -it laravel bin/bash를 입력하면 된다.
 >도커 초기 셋팅 끝
<br/>
<br/>

# Nginx 웹서버를 통해 laravel을 실행

<br/>
'''
// PHP TimeZone 질문 회피
export TZ=Asia/Seoul
ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
apt update && apt install -y php-fpm
'''
