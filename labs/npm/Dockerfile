FROM debian:stable
MAINTAINER Huei-Horng Yo <hiroshiyui@ecoworkinc.com>

ENV DEBIAN_FRONTEND=noninteractive TERM=xterm-256color

RUN apt-get update && apt-get install -y locales curl git tmux && apt-get clean

RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen && locale-gen
ENV LANG=en_US.UTF-8
ENV LC_ALL=en_US.UTF-8

RUN curl -sL https://deb.nodesource.com/setup_dev | bash -
RUN apt-get install -y nodejs

RUN npm config set loglevel verbose --global

RUN npm install -g bower
RUN npm install -g ember-cli
RUN npm install -g typescript

ADD index.js /root/
RUN mkdir /root/workspace
WORKDIR /root/workspace

CMD /bin/bash
