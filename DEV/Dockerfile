FROM ubuntu:20.04 as build
RUN apt update && DEBIAN_FRONTEND=noninteractive apt install -y tzdata
RUN apt install -y git default-jdk maven
WORKDIR /usr/local/src
RUN git clone https://github.com/koddas/war-web-project.git
RUN chmod -R 777 ./
WORKDIR /usr/local/src/war-web-project
RUN mvn package
