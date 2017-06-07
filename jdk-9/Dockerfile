FROM ubuntu:16.04
MAINTAINER Xiaoqi Cao <thomascxq@gmail.com>

#Install Oracle Java 9

RUN apt-get update \
    && apt-get -y install software-properties-common \
    && add-apt-repository -y ppa:webupd8team/java \
    && apt-get update \
    && echo oracle-java9-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections \
    && apt-get -y install oracle-java9-installer \
    && rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME /usr/lib/jvm/java-9-oracle
ENV PATH $JAVA_HOME/bin:$PATH
