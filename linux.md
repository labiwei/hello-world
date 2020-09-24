# .NET

## dotnetcore 3.1
参考文档:<https://docs.microsoft.com/zh-cn/dotnet/core/install/linux-centos#centos-7->

yum 命令如下

将 Microsoft 包签名密钥添加到受信任密钥列表

> sudo rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm

> sudo yum install aspnetcore-runtime-3.1

SDK包含运行时
<code>
sudo yum install dotnet-sdk-3.1
</code>

## .NET 5 
https://dotnetcli.blob.core.windows.net/dotnet/release/install-preview/install-dotnet-preview.sh
1. 创建下载文件夹,然后切换到该目录.
<code>
mkdir $HOME/dotnet_install && cd $HOME/dotnet_install
</code>

2. 下载sh安装脚本
<code>
curl -H 'Cache-Control: no-cache' -L https://aka.ms/install-dotnet-preview -o install-dotnet-preview.sh
</code>

3. 执行sh安装脚本
<code>
sudo bash install-dotnet-preview.sh
</code>

4. 校验安装结果
<code>
dotnet --info
</code>

## 卸载.NET
https://docs.microsoft.com/zh-cn/dotnet/core/install/remove-runtime-sdk-versions?pivots=os-linux#uninstall-net-core
<code>

yum remove dotnet-host

version="1.0.1"
sudo rm -rf /usr/local/share/dotnet/sdk/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.NETCore.App/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.AspNetCore.All/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.AspNetCore.App/$version
sudo rm -rf /usr/local/share/dotnet/host/fxr/$version
</code>


## nginx
ps -ef | grep nginx
cd /usr/sbin
./nginx -v
ps -C nginx -o pid
systemctl status  nginx
防火墙规则
iptables

守护进程 supervisor
EventListener

下载源
--
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

## 网卡驱动
https://blog.csdn.net/luhuaxiang/article/details/88396882