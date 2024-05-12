FROM ubuntu:18.04

RUN apt install git -y && apt install default-jdk -y
RUN apt install maven -y
#Download the project from GIT to the new directory
WORKDIR /usr/local/src
RUN git clone https://github.com/koddas/war-web-project.git
RUN chmod -R +x ./
#Transfer to project's directory where pom.xml + running maven
WORKDIR /usr/local/src/war-web-project
RUN mvn package