FROM php:fpm
COPY php.ini /usr/local/etc/php/
RUN apt-get update \
  && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libmcrypt-dev \
  && docker-php-ext-install pdo_mysql mysqli mbstring gd iconv

# php設定
RUN echo '\
date.timezone = "Asia/Tokyo"\n\
memory_limit = -1\n\
' >> /usr/local/etc/php/php.ini