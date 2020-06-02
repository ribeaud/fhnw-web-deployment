FROM openjdk:12-alpine

COPY roomreservation.war /

EXPOSE 8080

ENTRYPOINT java -Djava.security.egd=file:/dev/./urandom -jar /roomreservation.war