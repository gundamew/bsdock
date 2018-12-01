FROM mysql:5.7.22

ARG TZ=UTC

ENV TZ $TZ

RUN apt-get update \
    && apt-get install -y --no-install-recommends tzdata

COPY ./my.cnf /etc/mysql/conf.d

CMD ["mysqld"]
