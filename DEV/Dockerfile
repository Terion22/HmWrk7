FROM ubuntu:18.04
RUN apt update && \
    apt install git -y && \
    apt install default-jdk -y && \
    apt install maven -y
WORKDIR /tmp/boxfuse
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello.git
#RUN chmod -R 777 /tmp/boxfuse/boxfuse-sample-java-war-hello
WORKDIR /tmp/boxfuse/boxfuse-sample-java-war-hello
RUN mvn package
