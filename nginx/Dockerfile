FROM nginx:1.16.0

ARG TZ=UTC

ENV TZ $TZ

RUN rm /etc/nginx/conf.d/default.conf

COPY ./nginx.conf /etc/nginx

CMD ["nginx"]
