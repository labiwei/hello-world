# .NET

## linux系统环境

centos 7.8  
yum包管理器

## 网卡驱动

参考文档 > <https://blog.csdn.net/luhuaxiang/article/details/88396882>

## dotnetcore 3.1

参考文档 > <https://docs.microsoft.com/zh-cn/dotnet/core/install/linux-centos#centos-7->

yum 命令如下

```console
sudo rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm
sudo yum install aspnetcore-runtime-3.1
sudo yum install dotnet-runtime-3.1
sudo yum install dotnet-sdk-3.1
```

> :warning: 将 Microsoft 包签名密钥添加到受信任密钥列表
> :warning: SDK包含运行时

## .NET 5

参考文档 > <https://dotnetcli.blob.core.windows.net/dotnet/release/install-preview/install-dotnet-preview.sh>

1 创建下载文件夹,然后切换到该目录.

```console
mkdir $HOME/dotnet_install && cd $HOME/dotnet_install
```

2 下载sh安装脚本

```console
curl -H 'Cache-Control: no-cache' -L https://aka.ms/install-dotnet-preview -o install-dotnet-preview.sh
```

3 执行sh安装脚本

```console
sudo bash install-dotnet-preview.sh
```

4 校验安装结果

```console
dotnet --info
```

## 卸载.NET

参考文档 > <https://docs.microsoft.com/zh-cn/dotnet/core/install/remove-runtime-sdk-versions?pivots=os-linux#uninstall-net-core>

```console
yum remove dotnet-host

version="1.0.1"
sudo rm -rf /usr/local/share/dotnet/sdk/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.NETCore.App/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.AspNetCore.All/$version
sudo rm -rf /usr/local/share/dotnet/shared/Microsoft.AspNetCore.App/$version
sudo rm -rf /usr/local/share/dotnet/host/fxr/$version
```
