FROM openjdk:8-jdk-alpine
USER name
RUN wget https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.100/bin/apache-tomcat-8.5.100.tar.gz
RUN tar -xzvf apache-tomcat-8.5.100.tar.gz
RUN mv apache-tomcat-8.5.100 /opt/tomcat/
RUN rm apache-tomcat-8.5.100.tar.gz
RUN chmod +x /opt/tomcat/bin/*.sh

WORKDIR /opt/tomcat/webapps/manager
CMD ["/opt/tomcat/bin/catalina.sh","run"]