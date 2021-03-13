FROM php:8.0.1-fpm-alpine

WORKDIR /usr/src

RUN apk --no-cache update \
  && apk add autoconf build-base \
  && pecl install xdebug \
  && docker-php-ext-enable xdebug