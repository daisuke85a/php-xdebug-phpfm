FROM php:7.4.11-fpm-alpine3.12

COPY --from=composer /usr/bin/composer /usr/bin/composer

WORKDIR /usr/src/app

RUN docker-php-ext-install pdo_mysql

RUN apk --no-cache update \
  && apk add autoconf build-base \
  && pecl install xdebug \
  && docker-php-ext-enable xdebug

CMD sh -c "composer install && php artisan serve --host 0.0.0.0"