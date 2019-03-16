FROM php:7.2.15-fpm

RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install sockets
RUN docker-php-ext-install bcmath
RUN apt-get update -qq && \
    apt-get install -y -qq libzmq3-dev librabbitmq-dev
RUN pecl install zmq-beta \
    && docker-php-ext-enable zmq
RUN pecl install amqp \
    && docker-php-ext-enable amqp
RUN pecl install -o -f redis \
&&  rm -rf /tmp/pear \
&&  docker-php-ext-enable redis
RUN pecl install xdebug-2.6.0
RUN docker-php-ext-enable xdebug
RUN echo "xdebug.remote_enable=1" >> /usr/local/etc/php/php.ini

