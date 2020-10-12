# MariaDb

## 安装

```console
#安装源
curl -sS https://downloads.mariadb.com/MariaDB/mariadb_repo_setup | sudo bash
sudo yum install MariaDB-server galera-4 MariaDB-client MariaDB-shared MariaDB-backup MariaDB-common
sudo yum install MariaDB-server

systemctl start mariadb
systemctl enable mariadb
mysql_secure_installation
```

## 远程

```console
mysql
show databases;
use mysql;
show tables;
select Host,User,Password from user;
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '123456' WITH GRANT OPTION;
```

## 卸载

yum remove mariadb
ls /etc/my.cnf
ll /var/lib/mysql/
rm -rf /etc/my.cnf
rm -rf /var/lib/mysql/

## 防火墙

firewall-cmd --permanent --add-service=mysql
firewall-cmd --zone=public --add-port=3306/tcp --permanent
firewall-cmd --reload
