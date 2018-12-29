# Start with a base image containing Java runtime
FROM openjdk:8-jdk-alpine

# Add Maintainer Info
LABEL maintainer="marco.longobardi@eng.it"

# The application's jar file
ARG JAR_FILE=target/chapter3-spring-boot-1.0-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} chapter3-spring-boot.jar

# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/chapter3-spring-boot.jar"]