FROM php:7.2-apache

RUN apt-get update
RUN apt-get install -y libpng-dev

RUN docker-php-ext-install gd

RUN a2enmod rewrite
RUN a2enmod headers
RUN a2enmod expires

RUN apt-get clean
RUN rm -rf /var/lib/apt/lists/*
