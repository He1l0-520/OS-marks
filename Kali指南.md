# 树莓派 Kali 指南

## 换源

[Kali清华源](https://mirrors.tuna.tsinghua.edu.cn/help/kali/)

## 中文

### 安装字体

```shell
sudo apt install ttf-wqy-zenhei
```

### 更改语言设置

```shell
sudo dpkg-reconfigure locales
```

### 修改配置

```shell
sudo vim /etc/default/locale
```

修改内容

```
 LANG=zh_CN.UTF-8
 LC_ALL=zh_CN.UTF-8
```

### 输入法

```shell
sudo apt install ibus ibus-pinyin
```

## 🤔Kali好像基于Ubuntu，那[Ubuntu指南](./Ubuntu指南.mkd)也通用吧？
