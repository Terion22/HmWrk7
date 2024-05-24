FROM tomcat:8-alpine
USER root
RUN apk update
RUN apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64
RUN chmod 644 /opt/tomcat/bin/*.sh