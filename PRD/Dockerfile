FROM alpine:3.10 as buildp
RUN  apk update \
  && apk add git \
  && apk add maven \
  && apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64
WORKDIR /usr/local/src/war-web-project/target
FROM tomcat:9-jre8-temurin-focal
WORKDIR /usr/local/src/war-web-project/target/
COPY --from=buildp /usr/local/src/war-web-project/target/*.war /usr/local/tomcat/webapps/