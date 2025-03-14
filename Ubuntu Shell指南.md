# Ubuntu Shell指南

## 命令行颜色

```shell
PS1='\[\e[1;35m\]\u@\h:\[\e[0m\]\[\e[1;33m\]\w\[\e[1;35m\]\[\e[0m\]\[\e[1;34m\]\$ \[\e[0m\]'
```

## 网络开机超时

### 修改配置文件

```shell
sudo vim /etc/systemd/system/network-online.target.wants/systemd-networkd-wait-online.service
```

## 在[Service]下添加 TimeoutStartSec=2sec

```
TimeoutStartSec=2sec
```

## 换源

### x64/x86 [Ubuntu清华源](https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/)

### arm [Ubuntu清华源](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu-ports/)
