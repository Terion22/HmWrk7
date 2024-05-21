FROM openjdk:8-jdk-alpine
RUN  wget https://archive.apache.org/dist/tomcat/tomcat-8/v8.0.3/bin/apache-tomcat-8.0.3-deployer.tar.gz
RUN tar -xzvf apache-tomcat-8.0.3-deployer.tar.gz
RUN mv apache-tomcat-8.0.3-deployer /opt/tomcat
RUN rm apache-tomcat-8.0.3-deployer.tar.gz
RUN chmod 777 /opt/tomcat/bin/*.sh

CMD ["/opt/tomcat/bin/catalina.sh","run"]