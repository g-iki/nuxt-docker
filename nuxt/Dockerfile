FROM node:lts-alpine
# FROM node:15.2.1-alpine

ENV LANG=C.UTF-8 \
    TZ=Asia/Tokyo \
    APP_ROOT=/app

WORKDIR $APP_ROOT

RUN apk update && \
    apk upgrade && \
    apk add bash python make g++

RUN npm install yarn

ENV HOST 0.0.0.0
EXPOSE 3000