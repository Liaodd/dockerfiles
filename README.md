# dockerfiles

## 基本命令

从dockerfile构建image, 然后运行镜像的bash，以ubunut_mirror为例

```shell
$ cd ubunut_mirror

$ docker build -t liaodd/ubuntu .

$ docker run -i -t liaodd/ubuntu /bin/bash

```

## 这里有什么

### ubuntu_mirror 

从官方`ubuntu 14.04`构建一个镜像，并且把apt镜像设置为来自网易的镜像，提高速度

### php

从`ubuntu_mirror`构建一个php开发环境
