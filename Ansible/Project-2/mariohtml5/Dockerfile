FROM tomcat:9

MAINTAINER Prasanjit Singh //www.binpipe.org

RUN rm -rf /usr/local/tomcat/webapps/ROOT/*

ADD . /usr/local/tomcat/webapps/ROOT/

## Create non-root user 
RUN useradd -ms /bin/bash prasanjit \
    && usermod -aG prasanjit prasanjit \
    && chown -R prasanjit:prasanjit /usr/local/tomcat

EXPOSE 8080
CMD ["catalina.sh", "run"]

USER prasanjit
