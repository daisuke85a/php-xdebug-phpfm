FROM php:7.4.11-fpm-alpine3.12

WORKDIR /usr/src

RUN apk --no-cache update \
  && apk add autoconf build-base \
  && pecl install xdebug \
  && docker-php-ext-enable xdebug