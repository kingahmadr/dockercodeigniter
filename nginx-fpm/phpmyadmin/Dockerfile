FROM phpmyadmin/phpmyadmin:latest

RUN a2enmod ssl
RUN a2enmod rewrite
RUN cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/000-default.conf.orig
#RUN a2dissite 000-default.conf
#RUN a2dissite default-ssl.conf
#RUN a2ensite apache2-force-ssl.conf
#COPY ./phpmyadmin/ssl/phpmyadmin.crt /certs
#COPY ./phpmyadmin/ssl/phpmyadmin.key /certs
#COPY ./phpmyadmin/webconfig /etc/apache2/sites-available/
#RUN a2ensite apache2-force-ssl.conf

RUN sed -ri -e 's,80,443,' /etc/apache2/sites-available/000-default.conf
RUN sed -i -e '/^<\/VirtualHost>/i SSLEngine on' /etc/apache2/sites-available/000-default.conf
RuN sed -i -e '/^<\/VirtualHost>/i SSLCertificateFile /certs/phpmyadmin.crt' /etc/apache2/sites-available/000-default.conf
RUN sed -i -e '/^<\/VirtualHost>/i SSLCertificateKeyFile /certs/phpmyadmin.key' /etc/apache2/sites-available/000-default.conf
RUN sed -i -e '/^<\/VirtualHost>/i SSLCertificateChainFile /cert/fullchain.pem' /etc/apache2/sites-available/000-default.conf

EXPOSE 80 443
CMD ["apache2-foreground"]
