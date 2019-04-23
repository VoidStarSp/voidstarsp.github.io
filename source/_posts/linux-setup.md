---
title: linux-setup
date: 2019-04-23 11:14:36
tags:
---

## 1. guake
更好用的控制台
```
$ sudo apt install guake
```

## 2 .zsh && on-my-zsh
更好看的控制台
```
$ sudo apt-get install zsh
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

## 3. linux QQ
直接可用的AppImage
[linux QQ(包括QQ和TIM)](https://github.com/askme765cs/Wine-QQ-TIM)


## 4. sublime text
解决不能输入中文的问题
```
$ sudo apt-get update && sudo apt-get upgrade

$ git clone https://github.com/lyfeyaj/sublime-text-imfix.git
//切换到git目录
$ cd sublime-text-imfix

$ ./sublime-imfix
//need relogin
```

## 5. 桌面优化
提供一个系统监控面板
```
$ sudo apt-get install unity-tweak-tool
```
解压conky下Harmattan.zip到任意目录，移动.harmattan-assets到\~目录下。将.harmattan-themes下相应主题下(比如Ubuntu-Touch)God-Mode/normal-mode/.conkyrc移动到~目录，更改该文件窗口位置到想要的位置。

    在Startup Application添加开机启动，命令: conky -q

## 6. Docker
先更新apt
```
$ sudo apt update
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
在/etc/apt/sources.list.d/docker.list文件中添加下面内容
```
$ deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable
```
添加秘钥
```
$ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
再次更新apt
```
$ sudo apt update
```
安装docker-ce
```
$ sudo apt install docker-ce
```
add user group
```
$ sudo groupadd docker
$ sudo usermod -aG docker ${USER}
$ sudo systemctl restart docker
$ sudo su
$ sudo voidstar
```

## 7. Aria2
安装Aria2
```
$ sudo apt-get install aria2
```
配置
```
$ mkdir /usr/CodeWare/tools/aria2
$ cd /usr/CodeWare/tools/aria2  #切换工作目录
$ touch aria2.session           #新建session文件
$ vi aria2.conf                 #复制该配置文件到当前目录
```
启动
```
aria2c --conf-path=/usr/CodeWare/tools/aria2/aria2.conf -D
```
添加chrome配置

## 8.内网穿透
```
wget https://github.com/fatedier/frp/releases/download/v0.20.0/frp_0.20.0_linux_amd64.tar.gz
tar -zxvf frp_0.20.0_linux_amd64.tar.gz
cd frp_0.20.0_linux_amd64
rm -f frps
rm -f frps.ini
vi frpc.ini
```
[common]中的server_addr填frp服务端的ip[52.43.246.49]

## 9. 安装cuda之后显示器分辨率不能调节
更改/etc/X11/xorg.conf的配置(当前相应目录),reboot
```
$ sudo mv /etc/X11/xorg.conf /etc/X11/xorg.conf.backup
$ sudo mv xorg/xorg.conf /etc/X11/xorg.conf
$ reboot
```
切换nvidia driver冲突的时候
```
$
```

## 10. zsh下docker命令自动补全
https://www.cnblogs.com/zhuxiaoxi/p/8972980.html
