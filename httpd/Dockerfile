FROM ubuntu:16.04
RUN apt-get update && apt-get install -y apache2
ENV HTTPD_PREFIX /usr/local/apache2
ENV PATH $HTTPD_PREFIX/bin:$PATH
RUN mkdir -p "$HTTPD_PREFIX"\ 
	&& chown www-data:www-data "$HTTPD_PREFIX"
WORKDIR $HTTPD_PREFIX

COPY . /usr/local/apache2
EXPOSE 80
#RUN systemctl start apache2
CMD ["apache2ctl", "-D", "FOREGROUND"]
