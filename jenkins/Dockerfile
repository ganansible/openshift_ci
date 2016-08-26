FROM openshift/jenkins-1-centos7:latest

# Installing jenkins plugins.
COPY plugins.txt /opt/openshift/configuration/plugins.txt 
RUN /usr/local/bin/plugins.sh /opt/openshift/configuration/plugins.txt

# copy jobs
COPY jobs /opt/openshift/configuration/jobs
COPY jobs /var/lib/jenkins/jobs

#copy configuration 
COPY config.xml /opt/openshift/configuration/config.xml
COPY config.xml /var/lib/jenkins/config.xml

RUN sudo yum update
