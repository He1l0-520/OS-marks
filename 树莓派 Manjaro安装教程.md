# Manjaro安装教程

## 换源

```cmd
pacman-mirrors -i -c China -m rank
```

## 中文输入法

### 安装

```cmd
sudo pacman -S fcitx5 
sudo pacman -S fcitx5-configtool  
sudo pacman -S fcitx5-qt
sudo pacman -S fcitx5-gtk
sudo pacman -S fcitx5-chinese-addons
sudo pacman -S fcitx5-material-color
sudo pacman -S kcm-fcitx5
sudo pacman -S fcitx5-lua
```

### 配置

编辑~/.xprofile

```cmd
GTK_IM_MODULE DEFAULT=fcitx
QT_IM_MODULE  DEFAULT=fcitx
XMODIFIERS    DEFAULT=@im=fcitx
INPUT_METHOD  DEFAULT=fcitx
SDL_IM_MODULE DEFAULT=fcitxtx”
```

## 自动关机防熄灯断电

### 安装cronie

```cmd
sudo pacman -S cronie
```

### 设置计划

```cmd
crontab -e
```

![](C:\Users\琦\Pictures\EfG2i-BUMAAp_C1.jpeg)

### 启动服务

```cmd
sudo systemctl enable crond
sudo systemctl start crond
```

## 代理

### 安装clash

```cmd
sudo pacman -S clash
```

### 配置文件

将clash for windows的配置文件复制进`~/.config/clash`里面，记录文件开头的ip于端口，删除不需要的节点。

### 配置浏览器

安装FoxyProxy，在**选项-Proxies-添加**中添加代理设置，Hostname与端口写配置文件中对应的，保存后在插件中选中刚配置的代理。
