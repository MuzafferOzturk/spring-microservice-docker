FROM openjdk:8-jdk-alpine
ARG JAR_FILE=target/*.jar
VOLUME /tmp
EXPOSE 8765
COPY ${JAR_FILE} app.jar
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar" ]

#FROM openjdk:8-jdk-alpine
#ADD target/gateway-server-1.0-SNAPSHOT.jar gateway-server.jar
#ENTRYPOINT ["java", "-jar", "/gateway-server.jar"]
#EXPOSE 8765

#FROM openjdk:8-jdk-alpine
#ARG DEPENDENCY=target/dependency
#COPY ${DEPENDENCY}/BOOT-INF/lib /app/lib
#COPY ${DEPENDENCY}/META-INF /app/META-INF
#COPY ${DEPENDENCY}/BOOT-INF/classes /app
#ENTRYPOINT ["java","-cp","app:app/lib/*","tr.example.Application"]