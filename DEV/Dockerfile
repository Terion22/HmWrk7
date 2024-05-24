FROM ubuntu:18.04
USER root
#Solution of the problem of strict choosing timmezone
RUN apt update && DEBIAN_FRONTEND=noninteractive apt install -y tzdata
RUN apt update && \
    apt install git -y && \
    apt install default-jdk -y && \
    apt install maven -y
WORKDIR /tmp/boxfuse
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
RUN chmod -R 644 /tmp/boxfuse/boxfuse-sample-java-war-hello
WORKDIR /tmp/boxfuse/boxfuse-sample-java-war-hello
RUN mvn package
