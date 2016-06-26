# lazy_django

1. 도커 툴박스
  - https://www.docker.com/products/docker-toolbox

2. 우분투 도커 이미지 설치
  - docker pull ubuntu

3. pycharm 설치 (커뮤니티 버전) : 이미 유료버전 있는 분들은 그걸로~
  - https://www.jetbrains.com/pycharm/download/

4. 컨테이너 생성 스크립트 
  - https://github.com/psygrammer/lazy_django
  - create_lazy_django.sh 파일의 볼륨 설정을 자신에 맞게 바꿔준다.
  - 그리고 실행 
    - sh create_lazy_django.sh

4. 컨테이너 lazy_django 안으로 들어가서 (root 권한임)
  - apt-get update
  - apt-get install python
  - apt-get install python-pip
  - 장고 설치
    - pip install django
  - 위치 이동
    - cd /root/work
  - 장고프로젝트 생성
    - django-admin startproject hello
  - 프로젝트 디렉토리로 이동
    - cd hello
  - 장고 앱 생성
    - python manage.py startapp world
  - 개발용 서버를 실행시켜보자
    - pyhthon manage.py runserver 0.0.0.0:8000
  - 브라우저에서 -> http://192.168.99.100:8000/
    - 이때 IP는 도커 시스템에서 제공하는 매핑 IP (즉, 고래 모양이 나오고 그 밑에 나오는 IP를 쓰면 된다) 

5. student 라는 앱을 만들어서, 간단하게 REST API를 만드는 실습을 해보자
  - https://github.com/biospin/django
  - python manage.py startapp student
  - https://github.com/biospin/django/blob/master/apiSrv/student/views.py
  - https://github.com/biospin/django/blob/master/apiSrv/apiSrv/settings.py.1
  - https://github.com/biospin/django/blob/master/apiSrv/apiSrv/urls.py.1
