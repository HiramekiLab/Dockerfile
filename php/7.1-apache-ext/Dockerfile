FROM php:7.1-apache

RUN apt-get update \
  && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng12-dev libmcrypt-dev \
  && docker-php-ext-install pdo_mysql mysqli mbstring gd iconv mcrypt

RUN usermod -u 1000 www-data \
  && groupmod -g 1000 www-data

RUN a2enmod rewrite
