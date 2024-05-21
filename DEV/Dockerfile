FROM ubuntu:18.04
RUN apt update
RUN apt install -y git default-jdk maven
WORKDIR /tmp/koddas
RUN git clone https://github.com/koddas/war-web-project.git
RUN chmod -R 777 ./
WORKDIR /tmp/koddas/war-web-project
RUN mvn package
