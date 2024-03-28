---
layout: post
title:  "Welcome to Jekyll!"
date:   2024-03-28 10:29:00 +0900
categories: PostgreSQL
---

<h2>1. 데이터베이스 클러스터 생성</h2>

<!-- c:\Users\neon1\OneDrive\Workspace\pgsql\bin> -->
initdb.exe -U [USERNAME] -A password -W -E UTF8 c:\Users\neon1\OneDrive\Workspace\pgsql\[DATA FOLDER NAME]

initdb.exe : 데이터베이스 클러스터 초기화.
-U : 사용자 이름 설정. 부트스트랩 슈퍼 유저.
-A : 로컬 사용자 기본 인증 방법 지정. password로 지정.
-W : 비밀번호 설정 여부 메시지 표시.
-E : 템플릿 데이터베이스의 인코딩 선택. UTF8로 설정.
[DATA FOLDER NAME] : 데이터베이스 서버의 데이터 및 설정 저장 디렉토리 설정.

binary 폴더 경로에 data 폴더 생성되면 완료.

<h2>2. DB 프로세스 실행</h2>

<!-- c:\Users\neon1\OneDrive\Workspace\pgsql\bin> -->
pg_ctl start -D c:\Users\neon1\OneDrive\Workspace\pgsql\[DATA FOLDER NAME] -l c:\Users\neon1\OneDrive\Workspace\pgsql\logs\[LOG FILE NAME]

pg_ctl : 데이터베이스 클러스터 제어 유틸리티. 데이터베이스 서버의 시작, 중지, 재시작 및 상태 확인 가능
start : 데이터베이스 서버 시작.
stop : 데이터베이스 서버 중지. pg_ctl stop -D [DIRECTORY]
restart : 데이터베이스 서버 재시작. pg_ctl restart -D [DIRECTORY]
status : 데이터베이스 서버 상태 확인. pg_ctl status -D [DIRECTORY]
-D : 데이터베이스 데이터 디렉토리 경로.
-l : 데이터베이스 로그 기록. logs 폴더 생성 후 [LOG FILE NAME] 로그 생성 파일 이름 기재.

<h2>3. PostgreSQL 실행</h2>

pgAdmin4 폴더 내 runtime 폴더 내 pgAdmin4 실행
상단 메뉴에서 Object > Resiter 에서 [USERNAME], password 수정 또는 작성 후 저장.

