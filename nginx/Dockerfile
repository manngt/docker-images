FROM nginx

RUN useradd mauricio

COPY fruit /usr/share/nginx/html

ENV archivo docker

WORKDIR /usr/share/nginx/html

RUN echo "$archivo" > /usr/share/nginx/html/env.html

EXPOSE 90

LABEL version=1

USER mauricio

RUN echo "Yo soy $(whoami)" > /tmp/yo.html

USER root

RUN cp /tmp/yo.html /usr/share/nginx/html

VOLUME /var/log/ngnix

CMD nginx -g 'daemon off;'
