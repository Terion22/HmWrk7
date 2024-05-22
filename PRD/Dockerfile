FROM alpine:3.10
USER root
RUN apk update
RUN apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64

RUN wget https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.100/bin/apache-tomcat-8.5.100.tar.gz
RUN tar -xzvf apache-tomcat-8.5.100.tar.gz
RUN mv apache-tomcat-8.5.100 /opt/tomcat/
RUN rm apache-tomcat-8.5.100.tar.gz
RUN chmod +x /opt/tomcat/bin/*.sh

COPY /tmp/koddas/war-web-project/target/*war /usr/local/tomcat/webapps
WORKDIR /usr/local/tomcat/webapps
#CMD chmod +x /usr/local/tomcat/bin/catalina.sh
CMD ["/opt/tomcat/bin/catalina.sh","run"]
