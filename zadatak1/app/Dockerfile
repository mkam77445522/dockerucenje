FROM ubuntu:latest

RUN apt-get update && apt-get -y upgrade && DEBIAN_FRONTEND=noninteractive apt-get -y install \
    apache2 php php-mysql libapache2-mod-php curl lynx

RUN a2enmod php7.2
RUN a2enmod rewrite

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
#ENV APACHE_LOG_DIR /var/log/apache2
#ENV APACHE_LOCK_DIR /var/lock/apache2
#ENV APACHE_PID_FILE /var/run/apache2.pid

EXPOSE 80

ADD test.php /var/www/test.php

ADD apache-config.conf /etc/apache2/sites-enabled/000-default.conf


#RUN mkdir -p /opt/run/webphp/config
#RUN mkdir -p /opt/run/webphp/log

CMD /usr/sbin/apache2ctl -D FOREGROUND
