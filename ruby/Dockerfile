FROM alpine:3.4
MAINTAINER Dirk Siemers <dirk@sovido.de>

ENV BUILD_PACKAGES bash curl-dev ruby-dev build-base
ENV RUBY_PACKAGES ruby ruby-io-console ruby-bundler
ENV EXTRA_PACKAGES libxml2-dev libxslt-dev libev-dev libffi-dev git

# Update and install all of the required packages.
# At the end, remove the apk cache
RUN apk update && \
    apk upgrade && \
    apk add $BUILD_PACKAGES && \
    apk add $RUBY_PACKAGES && \
    apk add $EXTRA_PACKAGES && \
    rm -rf /var/cache/apk/*

RUN mkdir /usr/app
WORKDIR /usr/app
