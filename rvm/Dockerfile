FROM ubuntu:18.04

MAINTAINER John Ky <newhoggy@gmail.com>

ARG PID1_VERSION=0.1.0.1
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update                                                          && \
    apt-get -y install software-properties-common                           && \
    add-apt-repository ppa:rael-gc/rvm                                      && \
    apt-get -y remove --purge software-properties-common                    && \
    apt-get -y autoremove                                                   && \
    echo Done

RUN apt-get update                                                          && \
   apt-get -y install rvm                                                   && \
   apt-get -y install locales curl sudo git                                 && \
   rm -rf /var/lib/apt/lists/*
