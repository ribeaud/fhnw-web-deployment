FROM openjdk:12-alpine

COPY roomreservation.war /

ENTRYPOINT java -DdataSource.username=admin -DdataSource.password=Welcome2AWS -DdataSource.driverClassName=com.mysql.jdbc.Driver -DdataSource.url=jdbc:mysql://database-2.c23zxnhptcsn.eu-central-1.rds.amazonaws.com:3306/db -jar /roomreservation.war