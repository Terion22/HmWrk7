#FROM alpine:3.10 as buildp
#VOLUME /tmp/koddas/war-web-project/target
#RUN apk update \
#  && apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64
#WORKDIR /tmp/koddas/war-web-project/target

FROM tomcat:9.0-jdk13-openjdk-oracle
VOLUME /tmp/koddas/war-web-project/target
RUN cp /tmp/koddas/war-web-project/target/*.war /usr/local/tomcat/webapps.dist/manager
RUN cp -avT /usr/local/tomcat/webapps.dist/manager /usr/local/tomcat/webapps/manager
WORKDIR /usr/local/tomcat/webapps/manager
