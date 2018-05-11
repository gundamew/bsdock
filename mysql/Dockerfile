FROM mysql:5.7.22

ARG TZ=UTC

ENV TZ $TZ

RUN cp /usr/share/zoneinfo/$TZ /etc/localtime

COPY ./my.cnf /etc/mysql/conf.d

CMD ["mysqld"]
