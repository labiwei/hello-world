# Nginx

nginx的安装、命令、配置、进程、端口、填坑

## 安装

```console
sudo yum install nginx
```

> :warning: 添加 `nginx.repo` 地址 > [nginx源](http://nginx.org/en/linux_packages.html)

## 命令

```console
whereis nginx
```

## 配置

主配置文件: `cd /etc/nginx/nginx.conf`
子配置文件: `cd /etc/nginx/conf.d/*.conf`

默认: `default.conf` 基本上是80** 不使用
负载: `balance.conf`
守护: `supervisor.conf`
Web: `web.conf webapi.conf`

## 进程

```console
ps -ef | grep nginx
ps -C nginx -o pid
```

## 端口

```console
yum update firewall
firewall-cmd --zone=public --add-port=8080/tcp --permanent
firewall-cmd --zone=public --remove-port=8080/tcp --permanent
firewall-cmd --reload
firewall-cmd --zone=public --list-ports
```

## 参考
