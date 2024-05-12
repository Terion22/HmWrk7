FROM alpine:3.10 as buildp

RUN  apk update \
  && apk add git \
  && apk add maven \
  && apk  --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64/openjdk8-jdk-8.402.06-r0.apk
FROM tomcat:9-jre8-temurin-focal
COPY --from=buildp /usr/local/superproject/war-web-project/target/*.war /usr/local/tomcat/webapps/