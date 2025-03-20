# docker build -t jenkins-agent:nodejs .
# docker tag jenkins-agent:nodejs ghcr.io/pinklink-app/jenkins-agent:nodejs
# docker push ghcr.io/pinklink-app/jenkins-agent:nodejs
FROM ghcr.io/pinklink-app/jenkins-agent:base

USER root

RUN apt-get update && apt-get install -y curl && \
    curl -fsSL https://deb.nodesource.com/setup_20.x | bash - && \
    apt-get install -y nodejs && \
    npm install -g yarn && \
    rm -rf /var/lib/apt/lists/*

USER jenkins
