QingScan提供两种方式安装，
1、 开箱即用的docker版本，所有环境与依赖都已封装在镜像内，使用方便快捷。
2、 另一种是源代码安装方式，适用于开发者边开发边调试。

[TOC]

## docker版本安装

### 1. 安装docker
```
curl -sSL https://get.daocloud.io/docker | sh
```

![](images/20211203153747.png)

### 2. 安装docker-compose

安装compose命令如下：
```
sudo curl -L https://get.daocloud.io/docker/compose/releases/download/1.25.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
```
![](images/20211203154742.png)

众所周知的原因，国外的网站连接速度很慢。因此安装的时间可能会比较长，我们建议使用国内阿里云镜像
```
composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/
```

### 3. 添加可执行权限
```
sudo chmod +x /usr/local/bin/docker-compose
```

### 4. 下载QingScan
```
https://github.com/78778443/QingScan  
```

### 5. 拉去镜像并自动运行项目
进入20211014_01目录下,拉取镜像并自动启动项目
```
cd QingScan/docker/20211014_01 && docker-compose up
```
