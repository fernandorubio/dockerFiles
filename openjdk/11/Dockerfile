FROM ubuntu:focal

MAINTAINER Ferdinandpc "ferdinandpc@gmail.com"
 
ENV JAVA_HOME=/usr/local/java
ENV CLASSPATH=./:$JAVA_HOME/lib:$JAVA_HOME/jre/lib/ext
ENV PATH=$PATH:$JAVA_HOME/bin:$JAVA_HOME/jre/bin

RUN apt -qq update && apt -yqq install curl && apt -qq clean
RUN curl -s -L --url "https://download.java.net/java/GA/jdk11/9/GPL/openjdk-11.0.2_linux-x64_bin.tar.gz" | tar xz -C /usr/local \
&& ln -s /usr/local/11.0.2 /usr/local/java \
&& echo "JAVA_HOME=$JAVA_HOME" >> /etc/profile \
&& echo "CLASSPATH=./:\$JAVA_HOME/lib:\$JAVA_HOME/jre/lib/ext" >> /etc/profile \
&& echo "PATH=\$PATH:\$JAVA_HOME/bin:\$JAVA_HOME/jre/bin" >> /etc/profile \
&& echo "export PATH JAVA_HOME CLASSPATH" >> /etc/profile