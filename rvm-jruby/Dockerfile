FROM ubuntu:18.04

MAINTAINER John Ky <newhoggy@gmail.com>

ARG PID1_VERSION=0.1.0.1
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update                                                          && \
    apt-get -y install openjdk-8-jdk                                        && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install software-properties-common                           && \
    add-apt-repository ppa:rael-gc/rvm                                      && \
    apt-get -y remove --purge software-properties-common                    && \
    apt-get -y autoremove                                                   && \
    rm -rf /var/lib/apt/lists/*                                             && \
    echo Done

RUN apt-get update                                                          && \
    apt-get -y install rvm                                                  && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install git                                                  && \
    rm -rf /var/lib/apt/lists/*

RUN /bin/bash -l -c "rvm install jruby-1.7"
