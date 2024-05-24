FROM openjdk:6-jdk-alpine
USER root
RUN wget https://archive.apache.org/dist/tomcat/tomcat-7/v7.0.96/bin/apache-tomcat-7.0.96.tar.gz
RUN tar -xzvf apache-tomcat-7.0.96.tar.gz
RUN mv apache-tomcat-7.0.96 /opt/tomcat/
RUN rm apache-tomcat-7.0.96.tar.gz
RUN chmod +x /opt/tomcat/bin/*.sh
CMD ["/opt/tomcat/bin/catalina.sh","run"]