FROM debian

RUN apt update && apt install apache2 -y && apt clean

#ENV APACHE_LOCK_DIR="var/lock"
#ENV APACHE_PID_FILE="var/run/apache2.pid"
#ENV APACHE_RUN_USER="www-data"
#ENV APACHE_RUN_GROUP="www-data"
#ENV APACHE_LOG_DIR="var/log/apache2"

ENV APACHE_LOCK_DIR=/var/lock \
    APACHE_PID_FILE=/var/run/apache2/apache2.pid \
    APACHE_RUN_USER=www-data \
    APACHE_RUN_GROUP=www-data \
    APACHE_LOG_DIR=/var/log/apache2

ADD site.tar /var/www/html

LABEL description = "Apache Server"

VOLUME /var/www/html

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]
