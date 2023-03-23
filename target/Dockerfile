FROM maven:3.5-jdk-17 AS build  
ADD ./pom.xml pom.xml
ADD ./src src/
RUN mvn clean package

COPY --from=build target/allergy-service-1.0.0-SNAPSHOT.jar allergy-service-1.0.0-SNAPSHOT.jar  

FROM openjdk:17-jdk-alpine
EXPOSE 8081

ENTRYPOINT ["java","-jar","/AllergyService/target/allergy-service-1.0.0-SNAPSHOT"]