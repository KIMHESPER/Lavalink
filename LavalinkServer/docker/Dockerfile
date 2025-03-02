# Java 18 런타임 환경을 위한 Temurin 이미지 사용
FROM eclipse-temurin:18-jre-jammy

# non-root 사용자 추가 (보안을 위한 설정)
RUN groupadd -g 322 lavalink && \
    useradd -r -u 322 -g lavalink lavalink

# 작업 디렉토리 설정
WORKDIR /opt/Lavalink

# 파일 권한을 lavalink 사용자에게 변경
RUN chown -R lavalink:lavalink /opt/Lavalink

# non-root 사용자로 실행
USER lavalink

# Lavalink 서버의 JAR 파일 복사 (JAR 파일의 경로를 확인)
COPY LavalinkServer/build/libs/Lavalink.jar Lavalink.jar

# Lavalink 서버 실행을 위한 ENTRYPOINT 설정
ENTRYPOINT ["java", "-Djdk.tls.client.protocols=TLSv1.1,TLSv1.2", "-jar", "Lavalink.jar"]

# 포트 열기 (Lavalink 서버가 사용하는 포트)
EXPOSE 2333
