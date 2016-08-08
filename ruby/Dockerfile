FROM ruby:2.3.1-alpine
MAINTAINER Dirk Siemers <dirk@sovido.de>

# Update and install all of the required packages.
# At the end, remove the apk cache
RUN apk update && \
    apk upgrade && \
    apk add git && \
    rm -rf /var/cache/apk/*

RUN mkdir /usr/app
WORKDIR /usr/app
