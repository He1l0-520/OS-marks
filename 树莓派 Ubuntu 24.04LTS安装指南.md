# 树莓派 Ubuntu 24.04LTS安装指南

## 换源

[ubuntu-ports | 镜像站使用帮助 | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu-ports/)

## 固定ip

查看网络适配器信息

```shell
ip link show
```

查看网关

```shell
route -n
```

查看DNS

```shell
nslookup hcos
```

查找配置

```shell
cd /etc/netplan/
ls
```

修改配置

```shell
sudo vim /etc/netplan/
```

写入

```
# This file is generated from information provided by the datasource.  Changes
# to it will not persist across an instance reboot.  To disable cloud-init's
# network configuration capabilities, write a file
# /etc/cloud/cloud.cfg.d/99-disable-network-config.cfg with the following:
# network: {config: disabled}
network:
    version: 2
    wifis: 
        renderer: networkd
        wlan0:
            addresses: [192.168.137.100/24] #想要的地址
            routes:
              - to: default
                via: 192.168.137.1 #网关
            access-points:
                xiaomeizhijia: #wifi名
                    password: 4ca781025d70a71ed51a52ddbb2522996c37f29da77041c128751133d19fbfca #wifi密码
            dhcp4: false
            dhcp6: false
            optional: true
            nameservers: 
                addresses: [114.114.114.114]
                search: []
```

更新配置

```shell
sudo netplan apply
```

## 设置中文

```shell
sudo apt install language-pack-zh-hans
```

## 下载桌面

```shell
sudo apt install xfce4
```

## 安装opencv

```shell
sudo apt install libopencv-dev python3-opencv
```

## 安装vnc服务器

```shell
sudo apt install tightvncserver
```

## 启动vnc和桌面

```shell
vncserver :1
export DISPLAY=:1
startxfce4
```

## 变身！树莓派

```shell
sudo apt install raspi-config
```
