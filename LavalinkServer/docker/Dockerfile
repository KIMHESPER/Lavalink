# 기본 Java 이미지 사용
FROM openjdk:17-jre-slim

# Lavalink 디렉터리 생성
WORKDIR /opt/Lavalink

# Lavalink 파일 복사
COPY LavalinkServer/build/libs/Lavalink.jar /opt/Lavalink/Lavalink.jar

# Lavalink 서버의 기본 포트 및 IP 설정
EXPOSE 2333

# 실행할 명령어
ENTRYPOINT ["java", "-jar", "/opt/Lavalink/Lavalink.jar"]
