FROM centos
MAINTAINER Dongsu Jang <iolothebard@gmail.com>

RUN yum install -y tar

ENV JAVA_HOME /java
ENV PATH $JAVA_HOME/bin:$PATH
RUN mkdir -p "$JAVA_HOME"

ENV JDK_VERSION 8u45
ENV JDK_BUILD b14
RUN curl -L "http://download.oracle.com/otn-pub/java/jdk/$JDK_VERSION-$JDK_BUILD/jdk-$JDK_VERSION-linux-x64.tar.gz" -H 'Cookie: oraclelicense=accept-securebackup-cookie' | tar -xz --strip-components=1 --exclude='src.zip' --exclude='javafx-src.zip' --exclude='lib/missioncontrol' --exclude='lib/visualvm' -C "$JAVA_HOME"

RUN yum remove -y tar; yum clean all
