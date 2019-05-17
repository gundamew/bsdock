FROM php:7.3.5-fpm-stretch

ARG TZ=UTC
ARG PHP_TIMEZONE=UTC

ENV TZ $TZ

RUN echo "date.timezone=$PHP_TIMEZONE" > "$PHP_INI_DIR/conf.d/date-timezone.ini" \
    && docker-php-ext-install mysqli pdo_mysql

CMD ["php-fpm"]
