FROM node:alpine3.14

WORKDIR /bot/

RUN chmod 777 /bot

RUN apk add --no-cache --update \
      ca-certificates \
      git \
      bash \
      aria2 \
      wget \
      unzip \
      curl \
      unrar

ADD source.tar /bot/

RUN npm i -g typescript && \
    yarn && \
    tsc && \
    rm -rf src/.constants.js && \
    rm -rf out/.constants.js