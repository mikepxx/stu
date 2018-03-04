FROM ubuntu:16.04
WORKDIR /usr
RUN mkdir java
RUN mkdir tomcat
WORKDIR /usr/java 
RUN mkdirjdk
WORKDIR /usr/java/jdk
ADD /java/jdk1.8.0_144 /usr/java/jdk 
WORKDIR /usr/tomcat 
ADD /tomcat/apache-tomcat-8.0.45 /usr/tomcat

ENV JAVA_HOME=/usr/java/jdk
ENV JAVA_BIN=/usr/java/jdk/bin
ENV PATH=$PATH:$JAVA_HOME/bin
ENV CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
WORKDIR /usr/tomcat/webapps/ROOT
RUN rm -rf *
WORKDIR /usr
ADD stu.war /usr/tomcat/webapps/stu.war
EXPOSE 9999
CMD /usr/tomcat/bin/catalina.sh run