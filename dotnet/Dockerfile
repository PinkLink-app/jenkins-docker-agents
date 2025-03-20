# docker build -t jenkins-agent:dotnet .
# docker tag jenkins-agent:dotnet ghcr.io/pinklink-app/jenkins-agent:dotnet
# docker push ghcr.io/pinklink-app/jenkins-agent:dotnet
FROM ghcr.io/pinklink-app/jenkins-agent:base

USER root

RUN curl -fsSL https://packages.microsoft.com/config/debian/11/packages-microsoft-prod.deb -o packages-microsoft-prod.deb && \
    dpkg -i packages-microsoft-prod.deb && \
    rm packages-microsoft-prod.deb && \
    apt-get update && \
    apt-get install -y dotnet-sdk-8.0 aspnetcore-runtime-8.0 && \
    rm -rf /var/lib/apt/lists/*

ENV DOTNET_ROOT=/usr/share/dotnet
ENV PATH="$PATH:$DOTNET_ROOT"

USER jenkins
