FROM ubuntu:18.04

MAINTAINER John Ky <newhoggy@gmail.com>

ARG GHC_VERSION=8.0.2
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
    apt-get -y install locales curl sudo git                                && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install g++ libstdc++6                                       && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install libsnappy1v5 libtinfo-dev libsnappy-dev jq           && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install libz3-dev                                            && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install alex-3.1.7 cabal-install-2.4 happy-1.19.5            && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install hpack hspec-discover libyaml-0-2                     && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ghc-8.4.3                                            && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ghc-8.2.2                                            && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ghc-8.0.2                                            && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ghc-7.10.3                                           && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ghc-7.8.4                                            && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ghc-7.6.3                                            && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ghc-7.4.2                                            && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ghc-7.2.2                                            && \
    rm -rf /var/lib/apt/lists/*

RUN apt-get update                                                          && \
    apt-get -y install ghc-7.0.4                                            && \
    rm -rf /var/lib/apt/lists/*

RUN echo 'export PATH="$PATH:/opt/ghc/bin/"' >> /root/.bashrc

ENV LANG=C.UTF-8 \
    LC_ALL=C.UTF-8 \
    PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/bin:$PATH

RUN mkdir -p /root/.local/bin

RUN curl -L https://github.com/haskell-works/cabal-plan/releases/download/v0.5.0.0/cabal-plan_x86_64_linux.tar.gz -o cabal-plan_x86_64_linux.tar.gz     && \
    tar zxvf cabal-plan_x86_64_linux.tar.gz -C /root/.local/bin cabal-plan                                                                              && \
    rm cabal-plan_x86_64_linux.tar.gz

RUN curl -L https://github.com/haskell-works/cabal-cache/releases/download/v0.2.0.2/cabal-cache_x86_64_linux.tar.gz -o cabal-cache_x86_64_linux.tar.gz   && \
    tar zxvf cabal-cache_x86_64_linux.tar.gz -C /root/.local/bin ./cabal-cache                                                                            && \
    rm cabal-cache_x86_64_linux.tar.gz
