FROM ubuntu
ENV DEBIAN_FRONTEND noninteractive
RUN \
  apt update && \
  apt install apache2 php libapache2-mod-php php-cli php-cgi -y -q
COPY phpinfo.php /var/www/html
COPY apachecert.crt /etc/ssl/certs
COPY apachecert.key /etc/ssl/private
COPY ssl-config.conf /etc/apache2/sites-available
RUN a2enmod ssl
RUN a2ensite ssl-config
RUN cat /etc/apache2/sites-available/ssl-config.conf >> /var/www/html/sslvhost.txt
RUN service apache2 restart
EXPOSE 80 443
CMD apachectl -DFOREGROUND
