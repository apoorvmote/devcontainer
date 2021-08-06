# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.148.1/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version: bionic, focal
ARG VARIANT="focal"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends xz-utils

ENV PATH="$PATH:/usr/local/lib/nodejs/bin:\$PATH"

ENV NODE_VERSION=14.17.4

RUN sudo mkdir -p /usr/local/lib/nodejs/ \
    && wget https://nodejs.org/dist/v${NODE_VERSION}/node-v${NODE_VERSION}-linux-x64.tar.xz \
    && sudo tar -xf node-v${NODE_VERSION}-linux-x64.tar.xz -C /usr/local/lib/nodejs/ --strip-components=1 \
    && rm node-v${NODE_VERSION}-linux-x64.tar.xz

ENV TASK_VERSION=3.7.0

RUN wget https://github.com/go-task/task/releases/download/v${TASK_VERSION}/task_linux_amd64.deb \
    && dpkg -i task_linux_amd64.deb \
    && rm task_linux_amd64.deb

ENV PATH="$PATH:/usr/local/go/bin"

ENV GO_VERSION=1.16.7

RUN wget https://golang.org/dl/go${GO_VERSION}.linux-amd64.tar.gz \
    && tar -xf go${GO_VERSION}.linux-amd64.tar.gz \
    && sudo mv go/ /usr/local/ \
    && rm go${GO_VERSION}.linux-amd64.tar.gz

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && sudo ./aws/install \
    && rm awscliv2.zip

RUN npm install -g aws-cdk