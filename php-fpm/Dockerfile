FROM php:7.3.5-fpm-stretch

RUN apt-get update \
    && apt-get install -y \
        libzip-dev \
    && docker-php-ext-install mysqli pdo_mysql opcache zip

CMD ["php-fpm"]
