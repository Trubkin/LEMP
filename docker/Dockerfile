FROM php:7.4-fpm
RUN apt-get update && apt-get upgrade -y
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN curl --silent --show-error https://getcomposer.org/installer | php && \
    mv composer.phar /usr/local/bin/composer
# Uncomment to have mysqli extension installed and enabled
#RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
WORKDIR /var/www/html
CMD [ "php-fpm" ]

