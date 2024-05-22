FROM alpine:3.10
USER root
RUN apk update
RUN apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64

RUN wget https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.39/bin/apache-tomcat-9.0.39.tar.gz
RUN tar -xzvf apache-tomcat-9.0.39.tar.gz
RUN mv apache-tomcat-9.0.39 /opt/tomcat
RUN rm apache-tomcat-9.0.39.tar.gz
RUN chmod -R +x /opt/tomcat
RUN chmod -R 777 /usr/local/tomcat

CMD ["/opt/tomcat/bin/catalina.sh","run"]
