FROM tomcat:7.0-jre8

# add TEAM Engine webapp
ADD maven/dependency/teamengine-web-*.war /root/
RUN cd /root/ && unzip -q teamengine-web-*.war -d /usr/local/tomcat/webapps/teamengine

# add TEAM Engine common libs
ADD maven/dependency/teamengine-web-*-common-libs.zip /root/
RUN cd /root/ && unzip -q teamengine-web-*-common-libs.zip -d /usr/local/tomcat/lib

# add TEAM Engine console
ADD maven/dependency/teamengine-console-*-base.zip /root/
RUN cd /root/ && unzip -q teamengine-console-*-base.zip -d /root/te_base

# set TE_BASE
ENV JAVA_OPTS="-Xms1024m -Xmx2048m -DTE_BASE=/root/te_base"

# add ETS
ADD maven/ets-wfs10-*-ctl.zip /root/
RUN cd /root/ && unzip -q ets-wfs10-*-ctl.zip -d /root/te_base/scripts
ADD maven/ets-wfs10-*-deps.zip /root/
RUN cd /root/ && unzip -q -o ets-wfs10-*-deps.zip -d /usr/local/tomcat/webapps/teamengine/WEB-INF/lib

RUN cd /usr/local/tomcat/webapps/teamengine/WEB-INF/lib && cp xercesImpl*.jar -d /usr/local/tomcat/lib && rm -rf xercesImpl*.jar
RUN cd /usr/local/tomcat/webapps/teamengine/WEB-INF/lib && cp xml-apis*.jar -d /usr/local/tomcat/lib && rm -rf xml-apis*.jar

# run tomcat
CMD ["catalina.sh", "run"]