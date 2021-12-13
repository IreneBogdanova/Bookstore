FROM openjdk:17-jdk-alpine
VOLUME /main-app
ADD ./target/bookstore-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 8081
ENTRYPOINT ["java", "-jar","/app.jar"]