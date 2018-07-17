FROM docker:dind
LABEL maintainer="bryan.bialokur@gmail.com"

# Install Essentials
RUN apk update

# Install Packages
RUN apk add git && \
    apk add wget && \
	apk add openjdk8

ARG user=jenkins
ARG group=jenkins
ARG uid=1000
ARG gid=1000

ENV JENKINS_HOME /home/${user}

# Add Jenkins user
# Jenkins is run with user `jenkins`, uid = 1000
RUN addgroup -g ${gid} docker && \
    adduser -D -u ${uid} -G docker ${user}

# RUN chown -R ${user}:${user} /home/${user}

# Add the jenkins user to sudoers
RUN echo "${user}    ALL=(ALL)    ALL" >> etc/sudoers

# # Set Name Servers
# COPY /files/resolv.conf /etc/resolv.conf