# IMAGE LOADING
FROM rockylinux:9

# YUM PKG FILES - vsftpd, ftp
RUN yum -y update && yum -y install vsftpd ftp && yum clean all

# cp edited vsftpd.conf file
COPY vsftpd.conf.rockylinux9.template /etc/vsftpd/vsftpd.conf

VOLUME /var/ftp/pub
COPY WelcomeToMyFTPServer.txt /var/ftp/pub/WelcomeToMyFTPServer.txt
EXPOSE 21 20

ENTRYPOINT /usr/sbin/vsftpd


