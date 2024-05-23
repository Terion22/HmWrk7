FROM ubuntu:18.04
USER root
RUN apt update && \
    apt install git -y && \
    apt install default-jdk -y && \
    apt install maven -y
WORKDIR /tmp/koddas
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello
RUN chmod -R 777 /tmp/boxfuse
WORKDIR /tmp/boxfuse/boxfuse-sample-java-war-hello
RUN mvn package