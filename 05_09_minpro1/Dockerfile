# 베이스이미지
FROM rockylinux:9

# 패키지설치
# RUN yum -y update && yum -y install vsftpd && yum clean all
RUN yum -y install vsftpd && yum clean all

# conf파일 복사
COPY vsftpd.conf.rockylinux9.template /etc/vsftpd/vsftpd.conf

# mount volume 지정
VOLUME ["/var/ftp/pub"]
COPY WelcomeToMyFTPServer.txt /var/ftp/pub/WelcomeToMyFTPServer.txt

# 포트지정
EXPOSE 21 20

# 데몬기동 (foreground로 기동됨)
CMD ["/usr/sbin/vsftpd"]

