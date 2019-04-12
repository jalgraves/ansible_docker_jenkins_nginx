FROM jenkins/jenkins:2.172-alpine

USER root
RUN apk update && apk add docker shadow make py-pip
RUN apk add python-dev libffi-dev openssl-dev gcc libc-dev
RUN pip install --upgrade pip
RUN pip install docker-compose
RUN usermod -G ping -a jenkins

USER jenkins
# Change URL for use behind a reserve proxy
ENV JENKINS_OPTS "--prefix=/jenkins"

# Disable Jenkins automatic setup
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"

# Install plugins
COPY ./plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
