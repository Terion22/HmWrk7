FROM alpine:3.10 as buildp
RUN  apk update -y && \
     apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64 -y
#WORKDIR /tmp/koddas/war-web-project/target

FROM tomcat:9-jre8-temurin-focal
COPY --from=buildp /usr/koddas/war-web-project/target/*.war /opt/tomcat/webapps/