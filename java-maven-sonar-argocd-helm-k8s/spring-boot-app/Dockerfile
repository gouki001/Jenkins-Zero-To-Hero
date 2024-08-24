# Use the Eclipse Temurin image for Java 17
# FROM eclipse-temurin:17-jre-alpine
FROM maven:3.8.5-openjdk-17-slim

# Simply the artifact path
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

# Change ownership and permissions
RUN chown -R root:root /opt/app && chmod -R 777 /opt/app

COPY ${artifact} app.jar

# This should not be changed
ENTRYPOINT ["java","-jar","app.jar"]
