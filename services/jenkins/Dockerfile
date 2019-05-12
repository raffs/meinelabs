ARG JENKINS_VERSION

FROM jenkins/jenkins:${JENKINS_VERSION}

USER root

RUN apt-get update                               \
    && apt-get install -y build-essential curl   \
        git wget telnet maven gradle             \
        ruby ruby-dev python-dev golang          \
    && mkdir -p /mnt/logs                        \
    && chown -R jenkins:jenkins /mnt             \
    && echo "that's all folks"

USER jenkins
