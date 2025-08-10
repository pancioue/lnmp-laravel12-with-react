FROM php:8.4-fpm

RUN apt-get update && apt-get install -y \
    zip unzip curl \
    && docker-php-ext-install pdo_mysql

# app 安裝 react時也是要用到 node，其實可以跑單一容器即可
RUN curl -fsSL https://deb.nodesource.com/setup_24.x | bash - \
    && apt-get install -y nodejs=24.4.0-1nodesource1

# 加上 ll 指令
RUN echo "alias ll='ls -alF'" >> /root/.bashrc

# 安裝 Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www
