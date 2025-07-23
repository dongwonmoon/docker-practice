# 베이스 이미지
From python:3.11.6

# 작업 디렉토리 설정
WORKDIR /usr/src/app

# 호스트에 존재하는 파일을 도커 이미지의 파일 시스템 경로로 복사
COPY . .

# 이미지 빌드 시 실행할 명령어
RUN python -m pip install --upgrade pip
RUN pip install -r requirements.txt

# myapp 디렉토리로 이동
WORKDIR ./myapp

# CMD vs. RUN => RUN은 이미지 빌드 시 실행, CMD는 컨테이너 시작 시 실행
CMD gunicorn --bind 0.0.0.0:8000 myapp.wsgi:application
# 8000번 포트 열기
EXPOSE 8000