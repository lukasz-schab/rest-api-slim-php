FROM php:7.3-fpm@sha256:2d68e401d2d3b9f8a6572791cd7a25062450c43ff52e58391146809741ad0885

RUN apt-get -y update
RUN curl -L -C - --progress-bar -o /usr/local/bin/composer https://getcomposer.org/composer.phar
RUN chmod 755 /usr/local/bin/composer
RUN apt-get install -y git
RUN docker-php-ext-install pdo_mysql mysqli bcmath pcntl
RUN pecl install redis && docker-php-ext-enable redis
RUN echo "date.timezone=UTC" >> /usr/local/etc/php/conf.d/timezone.ini
RUN apt-get install -y wget nano
