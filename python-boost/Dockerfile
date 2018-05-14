from ubuntu:16.04

RUN apt-get update
RUN apt-get install -y 

RUN apt-get install --fix-missing -y \
    build-essential \
    wget \
    vim \
    python3 \
    python3-pip \
    libboost-dev \
    git \
    apt-file

RUN apt-get install --fix-missing -y \
    gcc \
    g++ \
    cmake \
    valgrind \
    pkg-config \
    uuid-dev \
    libcurl4-openssl-dev \
    libssl-dev \
    openssh-server \
    python-pip

RUN apt-file update

RUN apt-get install --fix-missing -y \
    inetutils-ping \
    inetutils-traceroute \
    net-tools \
    iptables \
    curl 
 
RUN pip3 install --upgrade pip 
# RUN link /usr/bin/python3 /usr/bin/python

RUN echo alias ls=ls >> /root/.bash_aliases
RUN chmod +777 /root/.bash_aliases

RUN printf "\
    set tabstop=4\n\
    set softtabstop=4\n\
    set expandtab\n\
    set showmatch\n\
    set shiftwidth=4\n\
    filetype plugin indent on\n\
    syntax off\n\
    " > ~/.vimrc
    
RUN apt-get install --fix-missing -y \
    llvm \
    clang-3.8 \
    clang

CMD bash

