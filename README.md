# dockerfiles

## 基本命令

从dockerfile构建image, 然后运行镜像的bash，以ubunut_mirror为例

```shell
$ cd ubunut_mirror

$ docker build -t liaodd/ubuntu .

$ docker run -i -t liaodd/ubuntu /bin/bash

```

## Base Image

### ubuntu_mirror 

从官方`ubuntu 14.04`构建一个镜像，并且把apt镜像设置为来自网易的镜像，提高速度

## App

### php

从`ubuntu_mirror`构建一个php开发环境。

使用下列命令启动环境

```shell
$ docker run -v /path/to/local/web/files:/app/web/default:rw -d -p 80:80 liaodd/php

# 在boot2docker中，可以使用如下命令访问
$ boot2docker ip

# 在主机通过浏览器输入以上的ip即可访问到boot2docker中的80端口
```
