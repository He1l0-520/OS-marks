# Ubnuntu指南

## 命令行

命令行颜色

```shell
PS1='\[\e[1;35m\]\u@\h:\[\e[0m\]\[\e[1;33m\]\w\[\e[1;35m\]\[\e[0m\]\[\e[1;34m\]\$ \[\e[0m\]'
```

## 网络开机超时

修改配置文件

```shell
sudo vim /etc/systemd/system/network-online.target.wants/systemd-networkd-wait-online.service
```

在[Service]下添加 TimeoutStartSec=2sec

```
TimeoutStartSec=2sec
```

## 换源

### x64/x86

[Ubuntu清华源](https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/)

### arm

[Ubuntu清华源](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu-ports/)

## JetBrain系列

### 1.Clion缺少编译器

`sudo apt install build-essential`

## 卸载应用

### 1.知道包名

`sudo apt-get remove --purge $软件名称`

`sudo apt-get autoremove --purge $软件名称`

### 2.不知道包名

`dpkg --get-selections | grep $软件关键词`

## Steam

### 1.闪退

安装第三方驱动，nvidia-driver-470

## Clash for Windows(已弃用）

### 1.挂了代理还是无法访问网络

打开系统设置-网络-网络代理。将`关`改为`手动`。
将http与https代理ip均改为`127.0.0.1`端口改为Clash常规设置中的端口号，默认为`7890`。

### 2.所有节点都超时

怀疑是dns问题。在配置页面，右键正在使用的配置文件，点击编辑。将

```
dns:
    enable: true
```

改为

```
dns:
    enable: false
```

注意每次更新配置文件后都要改一遍。

## IBus

### 1.安装拼音

`sudo apt-get install ibus-pinyin`

## 盒子

### 1.此电脑不符合windows最低安装要求

问题在于win11安全启动需要TPM硬件支持，而虚拟机没有。启动安装程序，前往修复计算机-疑难解答-启动命令行，运行**regedit**，找到`HKEY_LOCAL_MACHINE\SYSTEM\Setup`新建项命名为**LabConfig**，在**LabConfig**中新建**Dword (32-bit)值**BypassSecureBootCheck, BypassRAMCheck, BypassTPMCheck,**均赋值为1。**
关闭注册表，在命令行中运行**setup.exe**以启动安装程序。

### 2.如何绕过微软账号登陆

断网，在安装界面按**shift**与**F10**打开命令行。输入`oobe\BypassNRO.cmd`运行即可在安装时跳过微软账号登录。
