# docker-php-fpm-lighttpd

Container image with lighttpd, php-fpm and sqlite as web server serving Laravel/Lumen applications including PHP 7.1 and PHP 5.6 support.

### Examples

#### Dockerfile

```
FROM cyberduck/docker-php-fpm-lighttpd:php-5.6

# Copy source files to container
COPY . /var/www/localhost
RUN chown -R www-data. /var/www/localhost/
```

#### docker-compose

```
version: '2'
services:
    webserver:
        image: cyberduck/docker-php-fpm-lighttpd:php-7.1
        volumes:
            - ./lumen:/var/www/localhost
        ports:
            - "80:80"
```
