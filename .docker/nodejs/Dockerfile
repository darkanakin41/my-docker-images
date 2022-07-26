FROM node:lts-alpine3.15
LABEL maintainer="Pierre LEJEUNE <darkanakin41@gmail.com>"

RUN npm upgrade --global && npm install --global npm@latest

RUN npm config set prefix /home/node/.npm-packages
ENV PATH="${PATH}:/home/node/.npm-packages/bin"

RUN apk add --no-cache git

USER node 
WORKDIR /srv

VOLUME /srv
VOLUME /home/node/.cache
