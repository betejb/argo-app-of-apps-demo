# Docker file to build the java example container 
#
# Build stage
#
FROM maven:3.5.4-alpine AS build

COPY src /home/app/src

COPY pom.xml /home/app

RUN mvn -f /home/app/pom.xml clean package


#
# Package stage
#
FROM adoptopenjdk/openjdk11:jdk-11.0.8_10-alpine-slim

ARG JAR_FILE=target/*.jar

COPY --from=build /home/app/${JAR_FILE} app.jar

ENTRYPOINT ["java","-jar","/app.jar"]
