FROM gradle:latest AS BUILD
WORKDIR /usr/app/
COPY . . 
RUN gradle build

FROM openjdk:17-jdk-slim-buster

WORKDIR /Springboot
COPY . .


VOLUME /tmp
EXPOSE 8081
ADD /build/libs/demo-0.0.1-SNAPSHOT.jar demo-0.0.1-SNAPSHOT.jar
ENTRYPOINT ["java","-jar","demo-0.0.1-SNAPSHOT.jar"]
