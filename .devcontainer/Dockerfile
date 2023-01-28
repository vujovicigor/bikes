FROM php:7.2-apache 
MAINTAINER vujovichigor@gmail.com 
ENV APACHE_DOCUMENT_ROOT /workspace/bikes
RUN sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf
RUN sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf

#COPY php.ini /usr/local/etc/php/ # extension=mysql.so

#RUN apt-get update && apt-get install -y -o Dpkg::Options::="--force-confdef" libapache2-mod-php7  && a2enmod rewrite && service apache2 restart
RUN apt-get update && apt install git-all -y && a2enmod rewrite && service apache2 restart

EXPOSE 80