FROM ruby:2.4.1-alpine
MAINTAINER Dirk Siemers <dirk@sovido.de>

# Update and install all of the required packages.
# At the end, remove the apk cache
RUN apk update && \
    apk upgrade && \
    apk add git build-base libxml2-dev libxslt-dev qt5-qtwebkit-dev && \
    rm -rf /var/cache/apk/*

ENV QMAKE=/usr/lib/qt5/bin/qmake

RUN mkdir /usr/app
WORKDIR /usr/app
