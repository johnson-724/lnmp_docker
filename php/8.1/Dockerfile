FROM --platform=amd64 php:8.1

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN apt-get update && apt-get -y install vim

# Install Composer
# Install Composer
RUN chmod +x /usr/local/bin/install-php-extensions \
    && install-php-extensions @composer \
    && install-php-extensions rdkafka \
    && install-php-extensions redis \
    && install-php-extensions gd \
    && install-php-extensions zip \
    && install-php-extensions pdo \
    && install-php-extensions pdo_mysql \
    && install-php-extensions xdebug