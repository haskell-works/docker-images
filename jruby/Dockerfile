FROM ubuntu:18.04

MAINTAINER John Ky <newhoggy@gmail.com>

ARG PID1_VERSION=0.1.0.1
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update                                                          && \
    apt-get -y install zip                                                  && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install openssl                                              && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ubuntu-mono                                          && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install openjdk-11-jre                                       && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install jruby                                                && \
    rm -rf /var/lib/apt/lists/*

RUN gem install bundle
