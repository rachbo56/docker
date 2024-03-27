# 베이스이미지
FROM centos:7

# pkg 설치
RUN yum -y install httpd php && yum clean all

# volume 지정
VOLUME ["/var/www/html", "/var/log/httpd"]

# tar파일 복사 및 compress
ADD src.tar /var/www/html

# 포트지정
EXPOSE 80/tcp

# CMD로 도는 것 확인
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]


