# 1) 클라우딩 컴퓨팅 개요
## 클라우드 서비스의 종류
### IaaS(Infrastructure as a Service)
- 서버, 스토리지, 네트워크와 같은 인프라 하드웨어 자원을 제공
- 예) AWS의 EC2
### PaaS(Platform as a Service)
- 운영체제, 웹서버, 프레임워크 같은 플랫폼 서비스를 제공
- 예) Heroku
### SaaS(Software as a Service)
- 소프트웨어 서비스를 제공
- 예) 구글 앱서비스

# 2) 가상머신, 컨테이너, 도커, 쿠버네티스
## 가상머신
- 호스트 운영체제 위에 가상화 소프트웨어를 이용하여 여러 개의 게스트 OS를 구동
## 컨테이너
- 리눅스 기반의 물리적 공간 격리가 아닌 프로세스를 격리
- 운영체제의 커널을 공유하고 그 위에 파일들을 이미지로 빌드하여 패키지로 배포
## 도커
- 컨테이너를 잘 다룰 수 있게 도와주는 오픈소스 플랫폼
# 쿠버네티스
- 수많은 컨테이너의 관리작업을 자동화 해주는 오픈 소스 플랫폼