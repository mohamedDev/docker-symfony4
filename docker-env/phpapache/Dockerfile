FROM php:7.2-apache

MAINTAINER Mohamed BOUAZIZ

RUN apt-get update && \
    apt-get install -y apt-transport-https apt-utils curl git zlib1g-dev

RUN docker-php-ext-install zip

# Install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer


EXPOSE 80 443

WORKDIR /var/www/html/

CMD apachectl -D FOREGROUND