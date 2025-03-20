# docker build -t jenkins-agent:base .
# docker tag jenkins-agent:base ghcr.io/pinklink-app/jenkins-agent:base
# docker push ghcr.io/pinklink-app/jenkins-agent:base

FROM jenkins/inbound-agent:latest

USER root

RUN apt-get update && apt-get install -y openjdk-17-jdk && \
    rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64

USER jenkins

EXPOSE 50000
ENTRYPOINT ["/usr/local/bin/jenkins-agent"]
