FROM php:7.4-fpm

RUN curl -s https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer

RUN apt-get update && apt-get install -y curl libpq-dev libzip-dev zip unzip

RUN docker-php-ext-install pdo_pgsql zip

RUN pecl install xdebug
RUN docker-php-ext-enable xdebug

WORKDIR /app