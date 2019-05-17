FROM nginx:1.16.0

ARG TZ=UTC

ENV TZ $TZ

COPY ./nginx.conf /etc/nginx
COPY ./php-upstream.conf /etc/nginx/conf.d

CMD ["nginx"]
