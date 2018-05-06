FROM php:7.2.5-fpm-alpine3.7

ARG TZ=UTC
ARG PHP_TIMEZONE=UTC

ENV TZ $TZ

RUN apk update \
    && apk add --no-cache tzdata \
    && cp /usr/share/zoneinfo/$TZ /etc/localtime \
    && echo "date.timezone=$PHP_TIMEZONE" > "$PHP_INI_DIR/conf.d/date_timezone.ini" \
    && apk add --no-cache --virtual .build-deps $PHPIZE_DEPS \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug \
    && apk del .build-deps \
    && docker-php-ext-install pdo_mysql

CMD ["php-fpm"]
