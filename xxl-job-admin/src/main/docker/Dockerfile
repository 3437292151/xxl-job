FROM openjdk:8-jdk-alpine
ENV PROJECT_HOME /opt/project
# Add a jhipster user to run our application so that it doesn't need to run as root
RUN adduser -D -s /bin/sh jhipster
WORKDIR ${PROJECT_HOME}
ADD entrypoint.sh entrypoint.sh
RUN chmod 755 entrypoint.sh

ADD *.jar app.jar
ENTRYPOINT ["./entrypoint.sh"]
# ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/opt/project/app.jar"]
EXPOSE 8081 5701/udp