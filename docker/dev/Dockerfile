FROM node:10.13.0-alpine

LABEL MAINTAINER="Chigoziem Nwaiwu<princegoziem@gmail.com>"
LABEL application="fluido-backend"

ENV TERM=xterm-256color

WORKDIR /usr/app

RUN apk update && apk upgrade && \
  npm install -g yarn@1.12.x && rm -rf package-lock.json
COPY package.json /usr/app
COPY yarn.lock /usr/app

RUN yarn install
