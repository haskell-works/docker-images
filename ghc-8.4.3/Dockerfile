FROM ubuntu:18.04

MAINTAINER John Ky <newhoggy@gmail.com>

ARG LTS_SLUG=lts-10.1
ARG PID1_VERSION=0.1.0.1
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update                                                          && \
    apt-get -y install software-properties-common                           && \
    add-apt-repository ppa:hvr/ghc                                          && \
    apt-get -y remove --purge software-properties-common                    && \
    apt-get -y autoremove                                                   && \
    echo Done

RUN apt-get update                                                          && \
    apt-get -y install locales curl sudo                                    && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install libsnappy1v5 libtinfo-dev libsnappy-dev jq           && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    sudo apt-get -y install alex-3.1.7 cabal-install-2.2 happy-1.19.5       && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    sudo apt-get -y install ghc-8.4.3                                       && \
    rm -rf /var/lib/apt/lists/*

ENV LANG=C.UTF-8 \
    LC_ALL=C.UTF-8 \
    PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/bin:$PATH

RUN mkdir -p /root/.local/bin
