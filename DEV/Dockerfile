FROM ubuntu:18.04
RUN apt update
RUN apt install -y git default-jdk maven
WORKDIR /usr/koddas
RUN git clone http://github.com/koddas/war-web-project.git
WORKDIR /usr/koddas
RUN chmod -R 777 ./
WORKDIR /usr/koddas/war-web-project/
RUN mvn package