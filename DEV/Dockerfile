FROM ubuntu:18.04
RUN apt install git -y && \
    apt install default-jdk -y && \
    apt install maven -y

WORKDIR /usr/local/koddas
RUN git clone http://github.com/koddas/war-web-project.git
RUN chmod -R 644 .
#Transfer to project's directory where pom.xml + running maven
WORKDIR /usr/local/koddas/war-web-project/
RUN mvn package