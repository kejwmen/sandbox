FROM php:7.2-alpine

RUN apk add --no-cache \
    zlib-dev \
    g++ \
    autoconf \
    make \
    icu-dev

RUN docker-php-ext-install zip intl

RUN pecl install xdebug \
    && cp $(find /usr/local/lib/php/extensions/ -name xdebug.so) /usr/local/lib/php/extensions/xdebug.so

COPY ./php.ini  /usr/local/etc/php/conf.d/php.ini

WORKDIR /app

