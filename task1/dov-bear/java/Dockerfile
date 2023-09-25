# syntax=docker/dockerfile:1

FROM eclipse-temurin:17-jdk-jammy

WORKDIR /app

COPY .mvn/ .mvn
COPY mvnw pom.xml ./
RUN ./mvnw dependency:resolve

COPY src ./src

ENV APP_PORT=3000
EXPOSE ${APP_PORT}

ENTRYPOINT ["./mvnw", "spring-boot:run"]




