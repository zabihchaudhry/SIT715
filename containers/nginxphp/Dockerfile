FROM centos
MAINTAINER zabi@deakin.edu.au


RUN yum -y install epel-release;\
	yum -y install nginx;\
	yum clean all


COPY index.php /var/www/html/

# Export port 80
EXPOSE 80

# This container is a web server serving PHP apps, so a plain Apache is our entry point
ENTRYPOINT [ "/usr/sbin/nginx" ]
