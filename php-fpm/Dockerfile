FROM php:7.2.1-fpm-alpine3.7

ARG TZ=UTC
ARG PHP_TIMEZONE=UTC

ENV TZ $TZ

RUN apk update \
    && apk add --no-cache tzdata

RUN cp /usr/share/zoneinfo/$TZ /etc/localtime

RUN echo "date.timezone=$PHP_TIMEZONE" > "$PHP_INI_DIR/conf.d/date_timezone.ini"

CMD ["php-fpm"]

EXPOSE 9000
