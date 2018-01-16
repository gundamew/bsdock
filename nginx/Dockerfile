FROM nginx:1.13.8-alpine

ARG TZ=UTC

ENV TZ $TZ

RUN apk update \
    && apk add --no-cache tzdata

RUN cp /usr/share/zoneinfo/$TZ /etc/localtime

COPY ./nginx.conf /etc/nginx
COPY ./php-upstream.conf /etc/nginx/conf.d

CMD ["nginx"]

EXPOSE 80 443
