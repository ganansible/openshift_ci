FROM docker.io/fabric8/sti-karaf:latest
MAINTAINER docker-maven-plugin@jolokia.org
ENV DEPLOY_DIR=/opt/jboss/deploy
COPY maven /opt/jboss/deploy//
USER root
RUN ["chown", "-R", "jboss:jboss","/opt/jboss/deploy//"]

USER jboss
CMD /opt/karaf/bin/deploy-and-run.sh
