FROM alpine:3.10
USER root
RUN apk update
RUN apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64

RUN wget https://archive.apache.org/dist/tomcat/tomcat-6/v6.0.33/bin/apache-tomcat-6.0.33.tar.gz
RUN tar -xzvf apache-tomcat-6.0.33.tar.gz
RUN mv apache-tomcat-6.0.33 /usr/local/tomcat
RUN rm apache-tomcat-6.0.33.tar.gz

CMD ["/opt/tomcat/bin/catalina.sh","run"]
