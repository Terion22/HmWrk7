FROM alpine:3.10
USER root
RUN apk update
RUN apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64

RUN wget https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.100/bin/apache-tomcat-8.5.100.tar.gz
RUN tar -xzvf apache-tomcat-8.5.100.tar.gz
RUN mv apache-tomcat-8.5.100 /opt/tomcat/
RUN rm apache-tomcat-8.5.100.tar.gz
RUN chmod +x /opt/tomcat/bin/*.sh
WORKDIR /usr/local/tomcat/webapps
ADD /var/lib/docker/volumes/hmwrk7_c_vol/_data/wwp-1.0.0.war /usr/local/tomcat/webapps
CMD ["/opt/tomcat/bin/catalina.sh","run"]