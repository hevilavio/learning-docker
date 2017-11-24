FROM debian
LABEL Description="Webserver"

RUN apt-get update && apt-get install -y apache2 && apt-get clean

# RUN apt-get update && apt-get install -y apache

ENV APACHE_LOCK_DIR="/var/lock"
ENV APACHE_PID_FILE="/var/run/apache2.pid"
ENV APACHE_RUN_USER="www-data"
ENV APACHE_RUN_GROUP="www-data"
ENV APACHE_LOG_DIR="/var/log/apache"
ENV APACHE_RUN_DIR="/var/apache2"

VOLUME /var/www/html

EXPOSE 80

# iniciar o apache em foreground
ENTRYPOINT ["/usr/sbin/apache2", "-DFOREGROUND"]

