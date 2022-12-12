FROM openjdk:11.0-jre-slim
WORKDIR /app
COPY target/tlcdemoApp-1.0.0-SNAPSHOT-runner.jar /app/app.jar
EXPOSE 8080
CMD ["java", "-jar", "app.jar"]
