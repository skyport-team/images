FROM debian:bullseye-slim

RUN apt-get update && apt-get install -y \
    wget \
    php-cli \
    php-curl \
    php-xml \
    php-mbstring \
    php-zip \
    php-soap \
    php-gd \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app/data

CMD ["sh", "-c", "$START"]