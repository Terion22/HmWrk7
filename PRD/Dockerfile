FROM openjdk:8-jdk-alpine
USER root

RUN wget https://archive.apache.org/dist/tomcat/tomcat-6/v6.0.9/bin/apache-tomcat-6.0.9.tar.gz
RUN tar -xzvf apache-tomcat-6.0.9.tar.gz
RUN mv apache-tomcat-6.0.9 /opt/tomcat/
RUN rm apache-tomcat-6.0.9.tar.gz
RUN chmod +x /opt/tomcat/bin/*.sh
#WORKDIR /opt/tomcat/webapps
CMD ["/opt/tomcat/bin/catalina.sh","run"]