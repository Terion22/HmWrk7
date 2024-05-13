FROM alpine:latest as buildp
RUN  apk update \
  && apk add git \
  && apk add maven \
  && apk --n-cache add openjdk8 --repository=http://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64/openjdk8-8.402.06-r0.apk
WORKDIR /usr/local/tomcat/webapps/
FROM tomcat:9-jre8-temurin-focal
COPY --from=buildp /usr/local/src/war-web-project/target/*.war /usr/local/tomcat/webapps/