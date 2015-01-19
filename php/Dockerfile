FROM liaodd/ubuntu

MAINTAINER Liaodd, sglicx23@gmail.com

RUN apt-get update

RUN apt-get install nginx -y

RUN echo "daemon off;" >> /etc/nginx/nginx.conf

RUN rm /etc/nginx/sites-enabled/default

RUN apt-get install php5 php5-fpm php5-cli php5-mysql -y

ADD Add/index.php /app/web/default/index.php

ADD Add/nginx.default.conf /etc/nginx/conf.d/default.conf

ADD Add/supervisor.nginx.conf /etc/supervisor/conf.d/nginx.conf

ADD Add/supervisor.php5-fpm.conf /etc/supervisor/conf.d/php5-fpm.conf

EXPOSE 80

CMD ["/usr/bin/supervisord", "-n"]