FROM ubuntu:18.04
RUN apt update -y && \
    apt install git -y && \
    apt install default-jdk -y && \
    apt install maven -y
WORKDIR /tmp/koddas
RUN git clone http://github.com/koddas/war-web-project.git
WORKDIR /tmp/koddas
RUN chmod -R 777 /tmp/koddas
WORKDIR /tmp/koddas/war-web-project/
RUN mvn package