FROM alpine:latest

COPY ./repositories /etc/apk/

RUN apk add --no-cache php7 php7-fpm php7-mysqlnd php7-mbstring php7-pdo_mysql php7-redis \
    && rm -f /var/cache/apk/*

COPY ./php/www.conf /etc/php7/php-fpm.d
COPY ./php/php.ini /etc/php7/

EXPOSE 9000

CMD ["php-fpm7", "-F"]
