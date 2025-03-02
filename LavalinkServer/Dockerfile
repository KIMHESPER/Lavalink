FROM openjdk:17-jdk-alpine

WORKDIR /app
COPY . /app

RUN ./gradlew shadowJar

CMD ["java", "-jar", "Lavalink.jar"]
