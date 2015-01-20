# Dockerfiles

## 基本命令

从dockerfile构建image, 然后运行镜像的bash，以ubunut_mirror为例

```shell
$ cd ubunut_mirror

$ docker build -t liaodd/ubuntu .

$ docker run -i -t liaodd/ubuntu /bin/bash

```

## Base Image

### ubuntu_mirror (ubuntu 14.04)

从官方`ubuntu 14.04`构建一个镜像，并且把apt源设置为来自网易的镜像，提高速度。安装了后面依赖的supervisor

## App

### php (5.5)

从`ubuntu_mirror`构建一个`php 5.5`开发环境。

使用下列命令启动环境

```shell
$ cd php

$ docker build -t liaodd/php .

$ docker run -v /path/to/local/web/files:/app/web/default:rw -d -p 80:80 liaodd/php

# 在boot2docker中，可以使用命令获取vm的ip
# 在主机通过浏览器输入以上的ip即可访问到boot2docker中的80端口
$ boot2docker ip
```

### php53 (5.3)

从`ubuntu_mirror`构建一个`php 5.3`开发环境。

使用下列命令启动环境

```shell
$ cd php53

$ docker build -t liaodd/php53 .

$ docker run -v /path/to/local/web/files:/app/web/default:rw -d -p 80:80 liaodd/php53

# 在boot2docker中，可以使用命令获取vm的ip
# 在主机通过浏览器输入以上的ip即可访问到boot2docker中的80端口
$ boot2docker ip

```

### nodejs

从`ubuntu_mirror`构建一个`nodejs`开发环境。

使用下列命令启动环境

```shell
$ cd nodejs

$ docker build -t liaodd/nodejs .

$ docker run -v /path/to/local/web/files:/app/web/default:rw -d -p 80:80 liaodd/nodejs

# 在boot2docker中，可以使用命令获取vm的ip
# 在主机通过浏览器输入以上的ip即可访问到boot2docker中的80端口
$ boot2docker ip

```

## 官方资源

* [官方文档](http://docs.docker.com/)

## 官方以外的资源

### boot2docker 下载

* [百度盘](http://pan.baidu.com/s/1sjDKI7b) 

### 文章资源

* [Tanky Woo's blog: Docker 4 -- 总结](http://blog.tankywoo.com/docker/2014/05/08/docker-4-summary.html)

* [allengaller's list: Docker](http://segmentfault.com/bookmark/1230000000759382)

### images 镜像（mirror）

* [DAOCLOUD: 玩转Docker镜像](http://blog.daocloud.io/how-to-master-docker-image/)
