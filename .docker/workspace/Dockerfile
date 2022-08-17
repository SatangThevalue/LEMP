FROM composer:2.0

FROM php:8.0

ARG DEBIAN_FRONTEND=noninteractive
COPY --from=composer:2.0 /usr/bin/composer /usr/bin/composer
RUN apt-get update && apt-get install -y \
  software-properties-common locales
RUN apt-get update && apt-get install -y \
  git \
  curl \
  vim \
  nano \
  net-tools \
  pkg-config \
  iputils-ping \
  apt-utils \
  zip \
  unzip

RUN docker-php-ext-install \
  bcmath \
  pdo_mysql


# RUN curl -sL https://deb.nodesource.com/setup_14.x | bash

RUN apt-get install -y nodejs


RUN mkdir -p /var/www/html


COPY ./src /var/www/html