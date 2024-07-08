FROM mariadb

LABEL database = "studentapp"

WORKDIR /usr/local/bin/

ENV MARIADB_ROOT_PASSWORD=1234

COPY student-rds.sql /docker-entrypoint-initdb.d/

CMD ["mariadbd"]
