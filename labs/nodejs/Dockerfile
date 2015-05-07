FROM debian:stable
MAINTAINER Huei-Horng Yo <hiroshiyui@ecoworkinc.com>

ENV DEBIAN_FRONTEND=noninteractive TERM=vt220

RUN apt-get update && apt-get install -y curl npm && apt-get clean
RUN npm install -g npm && npm update -g && npm install -g bower

CMD /bin/bash
