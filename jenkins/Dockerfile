FROM jenkins/jenkins:lts

USER root
RUN apt update -y && \
    apt install -y python3-pip

RUN apt install -y rsync

RUN pip3 install awscli --upgrade

USER jenkins
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
