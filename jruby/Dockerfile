FROM ubuntu:18.04

MAINTAINER John Ky <newhoggy@gmail.com>

ARG PID1_VERSION=0.1.0.1
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update                                                          && \
    apt-get -y install zip                                                  && \
    echo Done

RUN apt-get update                                                          && \
    apt-get -y install openssl                                              && \
    echo Done

RUN apt-get update                                                          && \
    apt-get -y install ubuntu-mono                                          && \
    echo Done

RUN apt-get update                                                          && \
    apt-get -y install openjdk-11-jre                                       && \
    echo Done

RUN apt-get update                                                          && \
    apt-get -y install jruby                                                && \
    echo Done
