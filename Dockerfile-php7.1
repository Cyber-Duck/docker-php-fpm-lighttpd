FROM php:7.1.1-fpm-alpine

# Install php extensions
RUN apk update \
    && apk add lighttpd \
    && docker-php-ext-install mbstring opcache pdo pdo_mysql \
    && rm -rf /var/cache/apk/*

# Set the right timezone
RUN ln -snf /usr/share/zoneinfo/Etc/UTC /etc/localtime \
    && echo "UTC" > /etc/timezone

# Set the PHP config
RUN mkdir -p /usr/local/etc/php
COPY php.ini /usr/local/etc/php/php.ini

# Setup lighttpd config
COPY lighttpd.conf /etc/lighttpd/lighttpd.conf

#RUN chown -R www-data. /var/www/localhost/

WORKDIR /var/www/localhost
CMD php-fpm -D && lighttpd -D -f /etc/lighttpd/lighttpd.conf
