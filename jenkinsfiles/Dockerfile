FROM jenkins/jenkins:lts-alpine

USER root

RUN apk add --no-cache python3 \
    && ln -sf /usr/bin/python3 /usr/bin/python \
    && ln -sf /usr/bin/pip3 /usr/bin/pip

# Install other dependencies if needed
RUN apk add --no-cache pkgconf build-base python3-dev

# Install Jenkins plugins
USER jenkins

RUN jenkins-plugin-cli --plugins "blueocean docker-workflow"

