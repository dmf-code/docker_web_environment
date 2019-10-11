FROM php:7.0-fpm

WORKDIR /var/www

RUN apt-get update && apt-get install -y \
libfreetype6-dev \
libjpeg62-turbo-dev \
libpng-dev \
libmemcached-dev \
vim \
git \
&& docker-php-ext-install pdo_mysql \
&& docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
&& docker-php-ext-install gd \
&& docker-php-ext-install mysqli \
&& docker-php-ext-install bcmath
 
COPY ./composer /usr/local/bin/composer
ADD ./config/php.ini /usr/local/etc/php/php.ini


RUN chmod a+x /usr/local/bin/composer


EXPOSE 9000
