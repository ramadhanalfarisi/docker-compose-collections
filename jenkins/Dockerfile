FROM jenkins/inbound-agent:latest-jdk17

USER root
RUN apt-get update && apt-get install -y \
    wget \
    git \
    openjdk-17-jdk-headless && \
    wget https://go.dev/dl/go1.23.3.linux-amd64.tar.gz && \
    rm -rf /usr/local/go && tar -C /usr/local -xzf go1.23.3.linux-amd64.tar.gz && \
    rm go1.23.3.linux-amd64.tar.gz

ENV PATH=$PATH:/usr/local/go/bin

USER jenkins