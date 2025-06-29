# Ubuntu server 20.04 LTS

## 网络

[Linux wpa_cli 调试方法 - 江召伟 - 博客园](https://www.cnblogs.com/jiangzhaowei/p/8256920.html)

### 进入wpa_cli交互模式

```bash
sudo wpa_cli -i wlan0
```

### 指令

| 效果    | 指令                             |
| ----- | ------------------------------ |
| 扫描    | scan                           |
| 显示结果  | scan_result                    |
| 添加连接  | add_network <连接号>              |
| 设置网络名 | set_network <连接号> ssid <“网络名”> |
| 设置安全性 | set_network <连接号> key_mgmt <>  |
| 设置密码  | set_network <连接号> psk <"密码">   |
| 列出配置  | list_network                   |
| 启用配置  | enable_network <连接号>           |
| 删除网络  | remove_network                 |

## 颜色

[如何更改TTY的颜色？ colors - Dev59](https://dev59.com/askubuntu/r0PXs4cB2Jgan1zndAj4)

在`~/.bashrc`中添加如下内容

```bash
if [ "$TERM" = "linux" ]; then
    echo -en "\e]P0232323" #black
    echo -en "\e]P82B2B2B" #darkgrey
    echo -en "\e]P1D75F5F" #darkred
    echo -en "\e]P9E33636" #red
    echo -en "\e]P287AF5F" #darkgreen
    echo -en "\e]PA98E34D" #green
    echo -en "\e]P3D7AF87" #brown
    echo -en "\e]PBFFD75F" #yellow
    echo -en "\e]P48787AF" #darkblue
    echo -en "\e]PC7373C9" #blue
    echo -en "\e]P5BD53A5" #darkmagenta
    echo -en "\e]PDD633B2" #magenta
    echo -en "\e]P65FAFAF" #darkcyan
    echo -en "\e]PE44C9C9" #cyan
    echo -en "\e]P7E5E5E5" #lightgrey
    echo -en "\e]PFFFFFFF" #white
    clear #for background artifacting
fi
```

## 自动关机

[Crontab 在线生成器 | 菜鸟工具](https://www.jyshare.com/front-end/9444/)

### 打开crontab

```bash
sudo crontab -e
```

### 填写命令

```bash
15 22 * * * sudo -u root shutdown now
```
