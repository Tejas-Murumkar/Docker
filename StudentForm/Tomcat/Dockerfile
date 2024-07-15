
FROM ubuntu:latest

RUN apt update -y

RUN apt install openjdk-11-jdk -y

WORKDIR /opt/tomcat

EXPOSE 8080

ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.91/bin/apache-tomcat-9.0.91.tar.gz ./

RUN tar -xzf apache-tomcat-9.0.91.tar.gz -C ./

ADD https://studentwar.s3.ap-northeast-1.amazonaws.com/student.war ./apache-tomcat-9.0.91/webapps/

ADD https://studentwar.s3.ap-northeast-1.amazonaws.com/mysql-connector.jar ./apache-tomcat-9.0.91/lib

COPY context.xml ./apache-tomcat-9.0.91/conf/context.xml

CMD ["./apache-tomcat-9.0.91/bin/catalina.sh", "run"]
