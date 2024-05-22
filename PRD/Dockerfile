#FROM alpine:3.10 as buildp
#VOLUME /tmp/koddas/war-web-project/target
#RUN apk update \
#  && apk --n-cache add openjdk8 --repository=https://dl-cdn.alpinelinux.org/alpine/edge/community/x86_64
#WORKDIR /tmp/koddas/war-web-project/target

FROM FROM psmiraglia/tomcat8:8.5.13
USER root
RUN apk add --no-cache --update tzdata && rm -fr /var/cache/apk/*
ENV TZ=Europe/Rome

COPY /tmp/koddas/war-web-project/target/*.war ${TOMCAT_HOME}/webapps/
RUN chown -R ${TOMCAT_USER}:${TOMCAT_GROUP} ${TOMCAT_HOME}

USER ${TOMCAT_USER}

