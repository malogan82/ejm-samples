# Start with a base image containing Java runtime
FROM openjdk:8-jdk-alpine

# Add Maintainer Info
LABEL maintainer="marco.longobardi@eng.it"

# The payara's jar file
ARG JAR_FILE=target/payara-micro.jar

# The application's war file
ARG WAR_FILE=target/chapter3.war

# Add the payara's jar to the container
ADD ${JAR_FILE} payara-micro.jar

# Add the application's war to the container
ADD ${WAR_FILE} chapter3.war

# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/payara-micro.jar","--deploy","/chapter3.war"]