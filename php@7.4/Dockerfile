FROM php:7.4-fpm

RUN apt-get clean all && apt-get update && apt-get install -y
RUN apt-get install zlib1g-dev

RUN pecl install grpc protobuf
RUN docker-php-ext-enable grpc protobuf

RUN echo $(pwd)

WORKDIR /var/www/php
# ADD ./ /var/www/php
RUN echo $(ls /usr/local/etc/php)
# RUN cd /usr/local/etc/php/ && cp php.ini-production php.ini

EXPOSE 9000 8000
# CMD [ "php", "think" ,"run" ]
CMD [ "php-fpm" ]