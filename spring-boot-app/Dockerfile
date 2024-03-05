#Running build

FROM gcr.io/distroless/java

WORKDIR /opt/app

COPY target/spring-boot-web.jar .

ENTRYPOINT ["java","-jar","spring-boot-web.jar"]
