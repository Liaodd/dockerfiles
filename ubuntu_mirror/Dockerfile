FROM ubuntu:14.04

MAINTAINER Liaodd, sglicx23@gmail.com

RUN mv /etc/apt/sources.list /etc/apt/sources.list_bak \
&& echo deb http://mirrors.163.com/ubuntu/ trusty main restricted universe multiverse >> /etc/apt/sources.list \
&& echo deb http://mirrors.163.com/ubuntu/ trusty-security main restricted universe multiverse >> /etc/apt/sources.list \
&& echo deb http://mirrors.163.com/ubuntu/ trusty-updates main restricted universe multiverse >> /etc/apt/sources.list \
&& echo deb http://mirrors.163.com/ubuntu/ trusty-proposed main restricted universe multiverse >> /etc/apt/sources.list \
&& echo deb http://mirrors.163.com/ubuntu/ trusty-backports main restricted universe multiverse >> /etc/apt/sources.list \
&& echo deb-src http://mirrors.163.com/ubuntu/ trusty main restricted universe multiverse >> /etc/apt/sources.list \
&& echo deb-src http://mirrors.163.com/ubuntu/ trusty-security main restricted universe multiverse >> /etc/apt/sources.list \
&& echo deb-src http://mirrors.163.com/ubuntu/ trusty-updates main restricted universe multiverse >> /etc/apt/sources.list \
&& echo deb-src http://mirrors.163.com/ubuntu/ trusty-proposed main restricted universe multiverse >> /etc/apt/sources.list \
&& echo deb-src http://mirrors.163.com/ubuntu/ trusty-backports main restricted universe multiverse >> /etc/apt/sources.list

RUN apt-get update

RUN apt-get install -y supervisor