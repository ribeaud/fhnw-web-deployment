FROM openjdk:12-alpine

COPY roomreservation.war /

EXPOSE 8080

ENTRYPOINT java -Djava.security.egd=file:/dev/./urandom -DdataSource.username=admin -DdataSource.password=Welcome2AWS -DdataSource.driverClassName=com.mysql.jdbc.Driver -DdataSource.url=jdbc:mysql://database-2.c23zxnhptcsn.eu-central-1.rds.amazonaws.com:3306/db -jar /roomreservation.war