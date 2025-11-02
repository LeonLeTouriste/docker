#build
FROM maven:3.9.9-amazoncorretto-21 AS simple-api-build

#define directory and  enviroment
ENV SIMPLE_API_HOME=/opt/simple-api
WORKDIR $SIMPLE_API_HOME

#copy project files
COPY pom.xml .
COPY src ./src

#package application
RUN mvn package -DskipTests

#run
FROM amazoncorretto:21

#define directory and  enviroment
ENV SIMPLE_API_HOME=/opt/simple-api
WORKDIR $SIMPLE_API_HOME

#copy jar from build stage
COPY --from=simple-api-build $SIMPLE_API_HOME/target/*.jar $SIMPLE_API_HOME/simpleapi.jar

#command to run the application
ENTRYPOINT ["java", "-jar", "simpleapi.jar"]
