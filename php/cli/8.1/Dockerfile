FROM --platform=arm64 php:8.1

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN apt-get update && apt-get -y install vim

RUN chmod +x /usr/local/bin/install-php-extensions \
    && install-php-extensions @composer \
    rdkafka \
    redis \
    gd \
    zip \
    pdo \
    pdo_mysql \
    xdebug

WORKDIR /var/www/html