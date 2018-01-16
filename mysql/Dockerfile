FROM mysql:5.7.20

ARG TZ=UTC

ENV TZ $TZ

RUN cp /usr/share/zoneinfo/$TZ /etc/localtime

COPY ./my.cnf /etc/mysql/conf.d

CMD ["mysqld"]

EXPOSE 3306
