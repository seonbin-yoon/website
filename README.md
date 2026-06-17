# 웹 사이트 프로젝트

**간단한 소개**

내가 좋아하는 웹툰 작가들
작품 연재 안정도, 총 작품 갯수, 평균 화 분량
분석해서 리포트 만들어주는 사이트

## 사용 스택

- 프론트앤드: React
- 백앤드: Go
- DB: MySQL 8.0

## 개발환경 구축법

### 1. 필수 유틸 준비
- docker + docker compose가 깔려있어야 함.

### 2. 프로젝트 루트에 .env 파일 생성

#### 다음과 같이 작성하면 됩니다.
#### Go
- BACK_USER=... -> Go docker 유저 이름 **(필수)**
- BACK_PASSWORD=... -> Go docker 유저 비번 **(필수)**
#### MySQL
- DB_USER_NAME=... -> 도커 이미지 유저 이름 **(필수)**
- DB_USER_PASSWORD=... -> 도커 이미지 유저 비번 **(필수)**
- DB_ROOT_PASSWORD=... -> MySQL 루트 비번 **(필수)**
- DB_NAME=... -> 도커 이미지 빌드 후에 처음 생성할 DB이름 (선택)

### 3. Docker 이미지 빌드
- 프로젝트 루트 폴더에서 docker compose up --build -d 실행