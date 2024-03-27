# Docker base image
FROM centos:7

# pkg installation 
RUN yum -y install httpd mod_wsgi && yum clean all

# server setting
VOLUME /var/www/html /var/log/httpd
COPY vhost.conf /etc/httpd/conf.d
COPY myapp.wsgi /var/www/html/myapp.wsgi

# service up (foreground)
EXPOSE 80/tcp
CMD /usr/sbin/httpd -D FOREGROUND 



