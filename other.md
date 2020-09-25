# 其他

## nginx

    ps -ef | grep nginx
    cd /usr/sbin
    ./nginx -v
    ps -C nginx -o pid
    systemctl status nginx

## 防火墙

iptables -L

## 守护进程

supervisor

## 性能监控

EventListener

## MariaDb

    curl -sS https://downloads.mariadb.com/MariaDB/mariadb_repo_setup | sudo bash

安装源

`

sudo yum install MariaDB-server galera-4 MariaDB-client MariaDB-shared MariaDB-backup MariaDB-common
sudo yum install MariaDB-server
`
[超链接](http://www.foxtable.com/help/topics/0362.htm "超链接")
<https://www.cnblogs.com/miracle77hp/articles/11163532.html>
rpm -ivh --replacepkgs /home/dotnet_install/dotnet_packages/*

1、*.tar 用 tar -xvf 解压

2、*.gz 用 gzip -d或者gunzip 解压

3、*.tar.gz和*.tgz 用 tar -xzf 解压

4、*.bz2 用 bzip2 -d或者用bunzip2 解压

5、*.tar.bz2用tar -xjf 解压

6、*.Z 用 uncompress 解压

7、*.tar.Z 用tar -xZf 解压

8、*.rar 用 unrar e解压

9、*.zip 用 unzip 解压
