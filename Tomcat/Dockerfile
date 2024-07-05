FROM ubuntu:20.04

RUN apt update -y

RUN apt install  openjdk-11-jdk -y

WORKDIR /opt/tomcat

EXPOSE 8080 

ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.90/bin/apache-tomcat-9.0.90.tar.gz  /opt/tomcat

RUN tar -xzf apache-tomcat-9.0.90.tar.gz -C /opt/tomcat

ADD https://s3-us-west-2.amazonaws.com/studentapi-cit/student.war /opt/tomcat/apache-tomcat-9.0.90/webapps/

CMD ["apache-tomcat-9.0.90/bin/catalina.sh","run"]
