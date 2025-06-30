# 树莓派os指南

## 换源

[raspbian | 镜像站使用帮助 | 清华大学开源软件镜像站 | Tsinghua Open Source Mirror](https://mirrors.tuna.tsinghua.edu.cn/help/raspbian/)

## 设置中文

```shell
sudo apt install language-pack-zh-hans
```

## 摄像头??

修改配置文件

```shell
/etc/modules
```

在最下面添加

```shell
bcm2835-v4l2
```

检测摄像头

```shell
vcfencmd get_camera
```

## 安装opencv

```shell
sudo apt install python3-opencv
```
