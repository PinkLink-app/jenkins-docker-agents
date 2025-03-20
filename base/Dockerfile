FROM jenkins/inbound-agent:latest

USER root

# Install OpenJDK 17
RUN apt-get update && apt-get install -y openjdk-17-jdk && \
    rm -rf /var/lib/apt/lists/*

# Set Java Home environment variable
ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64

USER jenkins

EXPOSE 50000
ENTRYPOINT ["/usr/local/bin/jenkins-agent"]
