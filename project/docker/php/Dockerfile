FROM php:fpm

RUN apt-get update \
    && apt-get install -y libyaml-dev $PHPIZE_DEPS curl git unzip \
    && rm -rf /var/lib/apt/lists/*
    
RUN pecl install yaml && docker-php-ext-enable yaml

RUN curl -sS https://getcomposer.org/installer -o composer-setup.php \
    && php composer-setup.php --install-dir=/usr/local/bin --filename=composer \
    && rm composer-setup.ph