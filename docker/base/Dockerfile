FROM php:8.0.11-apache-buster

WORKDIR /var/www/expense/

RUN a2enmod rewrite

RUN apt-get update && apt-get install -y git unzip libicu-dev

RUN docker-php-ext-install \
    opcache \
    intl

COPY --from=composer:2.1.8 /usr/bin/composer /usr/bin/composer