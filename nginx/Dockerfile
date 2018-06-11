FROM nginx:1.15.0-alpine

ARG TZ=UTC

ENV TZ $TZ

RUN apk update \
    && apk add --no-cache tzdata \
    && cp /usr/share/zoneinfo/$TZ /etc/localtime

COPY ./nginx.conf /etc/nginx
COPY ./php-upstream.conf /etc/nginx/conf.d

CMD ["nginx"]
