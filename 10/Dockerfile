# link3tecnologia/wildfly:10
FROM link3tecnologia/centosjava8:7
ENV WILDFLY_VERSION=10.1.0.Final
ENV WILDFLY_FILE=wildfly-$WILDFLY_VERSION.tar.gz
WORKDIR /opt
RUN wget http://download.jboss.org/wildfly/$WILDFLY_VERSION/$WILDFLY_FILE
RUN tar xzf $WILDFLY_FILE
EXPOSE 8080 8443
RUN ln -s /opt/wildfly-$WILDFLY_VERSION /opt/wildfly
ENV LAUNCH_JBOSS_IN_BACKGROUND=true
CMD ["/opt/wildfly/bin/standalone.sh", "--server-config=standalone-full-ha.xml", "-b=0.0.0.0"]
