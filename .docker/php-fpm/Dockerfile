FROM php:8.0-fpm-alpine

# Install composer to /usr/local/bin/composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Type docker-php-ext-install to see available extensions
RUN docker-php-ext-install \
 bcmath \
 calendar \
 pdo \
 pdo_mysql


RUN mkdir -p /var/www/html

COPY ./src /var/www/html