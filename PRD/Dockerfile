FROM alpine:3.10
USER root
RUN apk update
RUN apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64

RUN wget https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.100/bin/apache-tomcat-8.5.100.tar.gz
RUN tar -xzvf apache-tomcat-8.5.100.tar.gz
RUN mv apache-tomcat-8.5.100 /opt/tomcat/
RUN rm apache-tomcat-8.5.100.tar.gz
RUN chmod +x /opt/tomcat/bin/*.sh

CMD ["/opt/tomcat/bin/catalina.sh","run"]


#FROM FROM psmiraglia/tomcat8:8.5.13
#USER root
#RUN apk add --no-cache --update tzdata && rm -fr /var/cache/apk/*
#ENV TZ=Europe/Rome

#COPY /tmp/koddas/war-web-project/target/*.war ${TOMCAT_HOME}/webapps/
#RUN chown -R ${TOMCAT_USER}:${TOMCAT_GROUP} ${TOMCAT_HOME}
#USER ${TOMCAT_USER}

