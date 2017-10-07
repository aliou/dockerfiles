FROM alpine:3.6
MAINTAINER Aliou Diallo <code@aliou.me>

RUN apk update
RUN apk add curl unzip bash
RUN curl -fsL https://github.com/bats-core/bats-core/archive/master.zip > bats.zip && \
      unzip bats.zip -d /opt/ && \
      mv /opt/bats-core-master/libexec/bats* /usr/local/bin/ && \
      chmod +x /usr/local/bin/bats* && \
      rm -rf /opt/bats-core-master /opt/bats.zip
RUN rm -rf /var/cache/apk/*
