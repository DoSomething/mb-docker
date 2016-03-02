# Message Broker composer base image.

FROM php:5.5-cli
MAINTAINER Sergii Tkachenko <sergii@dosomething.org>

# Packages
RUN apt-get update && \
  DEBIAN_FRONTEND=noninteractive apt-get install -y \
    zlib1g-dev \
    git \
  && rm -r /var/lib/apt/lists/* \
  && docker-php-ext-install mbstring bcmath zip \
  && curl -sS https://getcomposer.org/installer | \
      php -- --install-dir=/usr/local/bin --filename=composer

