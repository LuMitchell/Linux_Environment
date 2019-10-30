# Docker

*** 建议 不要用 root 操作

使用阿里云镜像 [地址](https://cr.console.aliyun.com/cn-hangzhou/instances/mirrors)
或其他镜像服务

> docker run --name mit-php-fpm -v ~/nginx/www/:/www --privileged=true -d php:7.2-fpm

## 遇到的问题

### php启动不了
启动之后马上就退出了，log 显示“Interactive shell”
内存足够，端口未占用。
后来 pull 指定的版本（7.2）就启动正常了，之前都是 pull 默认最新的。
问题还是不太明确
