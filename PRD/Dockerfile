FROM openjdk:8-jdk-alpine
RUN  wget https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.100/src/apache-tomcat-8.5.100-src.tar.gz
RUN tar -xzvf apache tomcat-8.5.100.tar.gz
RUN mv apache-tomcat-8.5.100 /opt/tomcat
RUN rm apache-tomcat-8.5.100.tar.gz
RUN chmod 777 /opt/tomcat/bin/*.sh

CMD ["/opt/tomcat/bin/catalina.sh","run"]