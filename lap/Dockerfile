FROM php:7.2-apache

RUN apt-get update
RUN apt-get install -y libpng-dev libxml2-dev

RUN docker-php-ext-install dom
RUN docker-php-ext-install gd
RUN docker-php-ext-install json
RUN docker-php-ext-install mbstring

RUN a2enmod rewrite
RUN a2enmod headers
RUN a2enmod expires

#CMD apachectl -k restart
