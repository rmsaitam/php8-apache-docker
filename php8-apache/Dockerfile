FROM php:8.0.1-apache-buster

ARG user
ARG uid

RUN docker-php-ext-install pdo pdo_mysql bcmath opcache 

RUN apt-get update && apt-get install -y \
    zlib1g-dev \
    libzip-dev
RUN docker-php-ext-install zip

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN a2enmod rewrite

COPY vhost.conf /etc/apache2/sites-available
RUN a2ensite vhost.conf


WORKDIR /var/www/html/crud-laravel

RUN useradd -G www-data,root -u $uid -d /home/$user $user
RUN mkdir -p /home/$user/.composer && \
    chown -R $user:$user /home/$user

USER $user

#RUN curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.35.3/install.sh | bash

#RUN source ~/.bashrc && nvm install v14.15.5
