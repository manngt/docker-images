FROM ubuntu
ENV DEBIAN_FRONTEND noninteractive
RUN apt update
RUN apt install apache2 -y -q
CMD apachectl -DFOREGROUND
