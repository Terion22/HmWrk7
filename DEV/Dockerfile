FROM ubuntu:20.04
RUN apt install git -y && apt install default-jdk -y && apt install maven -y
WORKDIR /usr/local/src
RUN git clone https://github.com/koddas/war-web-project.git
RUN chmod -R +x ./
#Transfer to project's directory where pom.xml + running maven
WORKDIR /usr/local/src/war-web-project
RUN mvn package