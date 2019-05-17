FROM mysql:5.7.22

ARG TZ=UTC

ENV TZ $TZ

COPY ./my.cnf /etc/mysql/conf.d

CMD ["mysqld"]
