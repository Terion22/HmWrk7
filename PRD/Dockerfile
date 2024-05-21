FROM alpine:3.10 as buildp
VOLUME /tmp/koddas/war-web-project/target
RUN apk update \
  && apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64
WORKDIR /tmp/koddas/war-web-project/target

FROM tomcat:9-jre8-temurin-focal
COPY --from=buildp /tmp/koddas/war-web-project/target/*.war /var/lib/tomcat9/webapps/
WORKDIR /var/lib/tomcat9/webapps/

CMD ["catalina.sh", "run"]