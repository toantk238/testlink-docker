FROM bitnami/php-fpm:7.4
LABEL maintainer="Toan-Tran toantk238@gmail.com"

WORKDIR /app
RUN mkdir -p /var/testlink/logs/
RUN chmod -R 777 /var/testlink/logs/
RUN mkdir -p /var/testlink/upload_area/
RUN chmod -R 777 /var/testlink/upload_area/

ADD ./testlink-code .

RUN chmod -R 777 /app/gui/templates_c/
# ADD ./entrypoint.sh /usr/bin/entrypoint.sh
# RUN chmod u+x /usr/bin/entrypoint.sh

RUN apt update && apt-get install -y php7.4-pgsql
RUN chmod -R 777 .

COPY ./php.ini /opt/bitnami/php/etc/php.ini

EXPOSE 9000
