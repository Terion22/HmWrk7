FROM ubuntu:18.04
USER root
RUN apt update && \
    apt install git -y && \
    apt install default-jdk -y && \
    apt install maven -y
WORKDIR /tmp/koddas
RUN git clone https://github.com/koddas/war-web-project.git
RUN chmod -R 777 /tmp/koddas
WORKDIR /tmp/koddas/war-web-project
RUN mvn package