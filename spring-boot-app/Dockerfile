#Build phase
FROM adoptopenjdk/maven-openjdk11:latest AS BUILD

WORKDIR /opt/app

COPY src ./src
COPY pom.xml .

RUN mvn clean package

#Running build

FROM gcr.io/distroless/java

WORKDIR /opt/app

COPY --from=BUILD /opt/app/target/spring-boot-web.jar .

ENTRYPOINT ["java","-jar","spring-boot-web.jar"]
