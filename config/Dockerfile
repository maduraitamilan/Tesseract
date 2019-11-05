# Start with a base image containing Java runtime
FROM openjdk:8-jdk-alpine

RUN apk update && apk add \
    tesseract-ocr \
    ghostscript

# The application's jar file
ARG JAR_FILE=target/tesseractmaster-v0.0.1.jar

# Add the application's jar to the container
ADD ${JAR_FILE} tesseractmaster-v0.0.1.jar

# Run the jar file 
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/tesseractmaster-v0.0.1.jar"]
