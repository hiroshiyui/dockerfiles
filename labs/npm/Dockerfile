FROM debian:stable
MAINTAINER Huei-Horng Yo <hiroshiyui@ecoworkinc.com>

ENV DEBIAN_FRONTEND=noninteractive TERM=vt220

RUN apt-get update && apt-get install -y locales curl npm && apt-get clean
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen && locale-gen
ENV LANG=en_US.UTF-8
ENV LC_ALL=en_US.UTF-8

RUN npm install -g npm && npm update -g && npm install -g bower

ADD index.js /root/

CMD /bin/bash
