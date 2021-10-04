FROM mariadb:10.6-focal

RUN touch /etc/my.cnf
COPY ./mariadb/.my.cnf /etc/my.cnf

EXPOSE 3306
CMD ["mysqld"]

