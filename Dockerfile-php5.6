FROM php:5.6.30-fpm-alpine

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

# Install Composer
RUN curl -s http://getcomposer.org/installer | php && \
    echo "export PATH=${PATH}:/var/www/localhost/vendor/bin" >> ~/.bashrc && \
    mv composer.phar /usr/local/bin/composer && \
    . ~/.bashrc

WORKDIR /var/www/localhost
CMD php-fpm -D && lighttpd -D -f /etc/lighttpd/lighttpd.conf
