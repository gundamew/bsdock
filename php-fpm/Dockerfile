FROM php:7.3.5-fpm-stretch

ARG TZ=UTC

ENV TZ $TZ

RUN echo "date.timezone=$TZ" > "$PHP_INI_DIR/conf.d/date-timezone.ini" \
    && docker-php-ext-install mysqli pdo_mysql opcache

CMD ["php-fpm"]
