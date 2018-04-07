FROM alpine:latest

COPY ./repositories /etc/apk/

RUN mkdir -p /run/nginx \
    && apk add --no-cache nginx \
    && rm -f /var/cache/apk/*

COPY ./nginx/default.conf /etc/nginx/conf.d/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
