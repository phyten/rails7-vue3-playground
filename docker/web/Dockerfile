FROM node:20.18.0-slim AS node

RUN npm install -g pnpm

FROM ruby:3.3.5-slim AS builder

COPY --from=node /usr/local/ /usr/local/
COPY --from=node /opt/ /opt/

RUN mkdir -p /myapp
WORKDIR /myapp

COPY . /myapp
