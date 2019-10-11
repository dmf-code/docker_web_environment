ARG mysql_version='5.7'
FROM mysql:$mysql_version

ENV MYSQL_ROOT_PASSWORD=root

COPY ./conf /etc/mysql/conf.d
COPY ./data /var/lib/mysql

EXPOSE 3306
