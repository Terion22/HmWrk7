FROM ubuntu:18.04
RUN apt update -y && \
    apt install git -y && \
    apt install default-jdk -y && \
    apt install maven -y

WORKDIR /tmp/koddas
RUN git clone http://github.com/koddas/war-web-project.git
RUN chmod -R 644 .
#Go to project's directory where pom.xml + running maven
WORKDIR /tmp/koddas/war-web-project/
RUN mvn package