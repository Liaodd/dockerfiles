FROM liaodd/ubuntu

MAINTAINER Liaodd, sglicx23@gmail.com

RUN apt-get update

RUN apt-get install nodejs npm -y

ADD Add/start.js /app/node/default/start.js

ADD Add/supervisor.nodejs.conf /etc/supervisor/conf.d/nodejs.conf

EXPOSE 80

CMD ["/usr/bin/supervisord", "-n"]