FROM node:8.6-alpine

MAINTAINER Ponkotsu <ponkotsu.ni@gmail.com>

RUN echo -e "@edge http://nl.alpinelinux.org/alpine/edge/main\n@testing http://nl.alpinelinux.org/alpine/edge/testing\n@community http://nl.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories

RUN apk -U add --no-cache \
    bash \
    git \
    openssh \
    python \
    sudo

RUN npm install -g typescript@2.2.0
RUN npm install -g @angular/cli

RUN adduser -D -u 801 docker \
    && echo "docker ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
USER docker

EXPOSE 4200
