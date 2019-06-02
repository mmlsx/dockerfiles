FROM docker.io/alpine:latest

RUN apk add --no-cach pcre-devel wget net-tools gcc zlib zlib-devel make openssl-devel

ADD http://nginx.org/download/nginx-1.16.0.tar.gz .
RUN tar zxvf nginx-1.16.0.tar.gz
RUN mkdir -p /usr/local/nginx
RUN cd nginx-1.16.0 && ./configure --prefix=/usr/local/nginx && make && make install
RUN rm -fv /usr/local/nginx/conf/nginx.conf
RUN mkdir -p /usr/local/nginx/conf/server

