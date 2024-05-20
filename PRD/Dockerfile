FROM openjdk:15-jdk-alpine
ENV TOMCAT_VERSION 10.1.19
RUN  apk update #&& \
    # apk add git && \
    # apk add maven && \

RUN wget -O /tmp/tomcat.tar.gz https://dlcdn.apache.org/tomcat/tomcat-10/v${TOMCAT_VERSION}/bin/apache-tomcat-${TOMCAT_VERSION}.tar.gz && \
    tar xf /tmp/tomcat.tar.gz -C /opt && \
    rm /tmp/tomcat.tar.gz && \
    mv /opt/apache-tomcat-${TOMCAT_VERSION} /opt/tomcat && \
    chmod 644 /opt/tomcat/bin/*sh

COPY /usr/local/war-web-project/target/wwp-1.0.0.war /opt/tomcat/webapps/
CMD ["catalina.sh", "run"]