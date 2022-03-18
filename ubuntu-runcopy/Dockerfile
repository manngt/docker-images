FROM ubuntu
LABEL version="1.0"
LABEL description="This is an apache image"
LABEL vendor="Orlando Perez"
ENV DEBIAN_FRONTEND noninteractive
RUN apt update
RUN apt install apache2 -y -q
WORKDIR /var/www/html
ENV contenido prueba
RUN echo ¨$contenido¨ > /var/www/html/prueba.html
ADD startbootstrap-freelancer-master .
COPY run.sh /run.sh
CMD sh /run.sh
