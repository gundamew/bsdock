FROM mysql:8.0.11

ARG TZ=UTC

ENV TZ $TZ

RUN cp /usr/share/zoneinfo/$TZ /etc/localtime

COPY ./my.cnf /etc/mysql/conf.d

CMD ["mysqld"]
