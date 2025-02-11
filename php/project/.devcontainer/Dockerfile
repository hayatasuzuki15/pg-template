FROM php:8.2-fpm

# システムの更新とGitのインストール
RUN apt-get update && \
    apt-get install -y \
    git \
    zip \
    unzip \
    libzip-dev \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# PHPの拡張機能をインストール
RUN docker-php-ext-install pdo_mysql zip

# Composerのインストール
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# 作業ディレクトリの設定
WORKDIR /var/www/html

# ... 既存のPHP関連の設定 ...