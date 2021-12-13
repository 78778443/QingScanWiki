
## 两种方式安装，
1、 开箱即用的docker版本，所有环境与依赖都已封装在镜像内，使用方便快捷。
2、 另一种是源代码安装方式，适用于开发者边开发边调试。

[TOC]

## 视频安装教程

[QingScan视频安装教程](https://www.bilibili.com/video/BV1wP4y1G74V)


## 1. 安装docker
```
curl -sSL https://get.daocloud.io/docker | sh
```

![](images/20211203153747.png)

## 2. 安装docker-compose

安装compose命令如下：
```
sudo curl -L https://get.daocloud.io/docker/compose/releases/download/1.25.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
```
![](images/20211203154742.png)

设置可执行权限
```
sudo chmod +x /usr/local/bin/docker-compose
```

## 3. 下载QingScan
```
https://github.com/78778443/QingScan  
```

## 4. 拉去镜像并自动运行项目
进入20211014_01目录下,拉取镜像并自动启动项目
```
cd QingScan/docker/20211014_01 && docker-compose up -d
```
## 5. 启动内置MySQL数据库
```
docker exec qingscan sh -c 'service mysql start'
```
接下来通过浏览器去访问URL地址：`http://host:8000/` 

用户名：`test1` 密    码：`123456`

![](images/20211206164654.png)
