FROM nginx:1.13.8-alpine

COPY ./nginx.conf /etc/nginx
COPY ./php-upstream.conf /etc/nginx/conf.d

CMD ["nginx"]

EXPOSE 80 443
