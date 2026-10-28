\# 개발자 작업실 구축 미션



\## 1. 프로젝트 개요

Docker를 이용해 웹 서버를 실행하고 브라우저에서 접속하는 개발 환경을 구축했다.



\## 2. 사용 환경

\- 운영체제: Windows

\- 버전 관리: Git

\- 컨테이너 실행 환경: Docker Desktop

\- 웹 서버: Nginx



\## 3. 프로젝트 구성

\- `Dockerfile`: 웹 서버 이미지 생성 설정

\- `app/index.html`: 웹 페이지 파일



\## 4. 실행 및 검증

1\. Docker 이미지를 `my-dev-web` 이름으로 빌드했다.

2\. `my-dev-container` 컨테이너를 실행했다.

3\. 포트 8081을 통해 웹 서버에 접속했다.

4\. 브라우저에서 직접 작성한 웹 페이지가 표시되는 것을 확인했다.



\## 5. 사용한 주요 명령어

```powershell

git --version

docker --version

docker images

docker ps -a

docker build -t my-dev-web .

docker run -d --name my-dev-container -p 8081:80 my-dev-web

```



\## 6. 트러블슈팅

\### 문제 1. Dockerfile 이름 오류

\- 문제: 파일이 `Dockerfile.txt`로 저장되어 있었다.

\- 원인: 파일 이름에 `.txt` 확장자가 추가되었다.

\- 해결: 파일 이름을 `Dockerfile`로 변경했다.



\### 문제 2. 웹 서버 접속 실패

\- 문제: `localhost:8081`에 접속할 수 없었다.

\- 확인: `docker ps -a`에서 새 컨테이너가 생성되지 않은 것을 확인했다.

\- 해결: Dockerfile을 확인하고 이미지를 빌드한 다음 컨테이너를 실행했다.



\## 7. 결과

Docker 이미지를 생성하고 컨테이너를 실행하여 웹 페이지 접속에 성공했다.

