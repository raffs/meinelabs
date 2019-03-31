ARG JENKINS_VERSION

FROM jenkins/jenkins:${JENKINS_VERSION}

USER root

RUN mkdir -p /mnt/logs                 \
    && chown -R jenkins:jenkins /mnt

USER jenkins
