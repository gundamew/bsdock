FROM php:7.2.1-fpm-alpine3.7

RUN docker-php-ext-install pdo_mysql

ARG TZ=UTC
ARG PHP_TIMEZONE=UTC

ENV TZ $TZ

RUN apk update \
    && apk add --no-cache tzdata \
    && cp /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo "date.timezone=$PHP_TIMEZONE" > "$PHP_INI_DIR/conf.d/date_timezone.ini"

RUN apk add --no-cache $PHPIZE_DEPS \
    && pecl install xdebug-2.6.0beta1 \
    && docker-php-ext-enable xdebug

CMD ["php-fpm"]

EXPOSE 9000
