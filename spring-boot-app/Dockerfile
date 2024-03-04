#Running build

FROM gcr.io/distroless/java

WORKDIR /opt/app

COPY spring-boot-app/target/spring-boot-web.jar .

ENTRYPOINT ["java","-jar","spring-boot-web.jar"]
