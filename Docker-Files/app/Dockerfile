FROM openjdk:11 AS BUILD_IMAGE
LABEL "Project"="jbhinfo"
LABEL "Author"="JBH"
RUN apt update && apt install maven -y
RUN git clone https://github.com/JJansenHansen/jbhinfo.net.git
RUN cd jbhinfo.net && mvn install

FROM tomcat:9-jre11
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE jbhinfo.net/target/jbhinfo-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]
