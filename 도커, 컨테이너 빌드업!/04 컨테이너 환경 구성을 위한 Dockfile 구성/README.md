# 1) 코드로 개발하는 컨테이너 인프라, Dockerfile
## IaC (Infrastructure as Code)
- 인프라 구축을 스크립트화 하여 자동화 하는 것
## Dockerfile
- 특정 컨테이너에 대한 모든 설정 내용을 담은 파일로, 도커 이미지를 생성함

# 2) Dockerfile 명령어와 이미지 빌드
## Dockerfile 작성 시 권장 사항
### 명령어 FROM
- 이미지를 선택할 때 작은 크기의 이미지(slim)와 리눅스 배포판인 알파인(Alpine) 이미지를 권장
### 명령어 RUN
- 다단계 빌드 사용과 각 이미지별로 개별 Dockerfile로 빌드 권장
### 명령어 COPY
- COPY는 RUN 명령어 이후에 작성하는 것을 권장
- 필요한 부분만 COPY를 권장
## 이미지 빌드 과정
- 도커 이미지는 Dockerfile의 명령어 단위로 실행할 때마다 읽기 전용 레이어를 생성하여 최종 이미지로 생성됨
- 빌드 캐시 : docker build는 빌드 속도 향상을 위해 실행 중간에 있는 이미지 캐시를 사용