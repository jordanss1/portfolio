FROM php:8.3-fpm

RUN groupadd -g 101 php-fpm \
    && useradd --no-log-init -u 101 -g 101 php-fpm \
    && chown php-fpm:php-fpm -R /var/www/html

RUN apt-get update && \
    apt-get install 

USER php-fpm

WORKDIR /var/www/html   

COPY php.ini /usr/local/etc/php/

COPY --chown=php-fpm . /var/www/html/