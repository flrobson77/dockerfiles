FROM debian:7

RUN apt-get update && apt-get install -y apache2 && apt-get clean

ENV APACHE_LOCK_DIR="/var/lock"
ENV APACHE_PID_FILE="/var/run/apache2.pid"
ENV APACHE_RUN_USER="www-data"
ENV APACHE_RUN_GROUP="www-data"
ENV APACHE_LOG_DIR="/var/log/apache2"

LABEL Description="WEBSERVER"

VOLUME /var/www/html

EXPOSE 80

ENTRYPOINT ["/usr/bin/apache2ctl", "-D", "FOREGROUND"]

