FROM ubuntu:16.04
ADD exsh.sh /usr/local/sbin
RUN chmod 777 /usr/local/sbin/exsh.sh && exsh.sh
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello && cd boxfuse-sample-java-war-hello && mvn package
RUN cp boxfuse-sample-java-war-hello/target/hello-1.0.war /usr/local/tomcat/webapps/
EXPOSE 8080
CMD /usr/local/tomcat/bin/catalina.sh run



