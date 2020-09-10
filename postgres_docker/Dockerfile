FROM postgres:10

RUN apt-get update && apt-get install -y \
      openssl \
      curl \
      postgresql-server-dev-10 \
      pgxnclient \
      make \
      gcc && \
    pgxnclient install temporal_tables && \
    apt-get autoremove -y
    
COPY psql.conf /etc/postgresql/postgresql.conf
COPY setup_sormas.sh /docker-entrypoint-initdb.d/

