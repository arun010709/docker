FROM eclipse-temurin:17-jdk-jammy
WORKDIR /spring-boot-app
COPY cert.txt /spring-boot-app
COPY target/spring-docker.jar /spring-boot-app
EXPOSE 8181
CMD ["java","-jar","spring-docker.jar"]
