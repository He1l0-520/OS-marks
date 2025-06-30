# Manjaro-arm-install

##  安装前准备

[Manjaro Forum](https://forum.manjaro.org/t/install-manjaro-on-pi5/175626)

[Gitlab](https://gitlab.manjaro.org/manjaro-arm/applications/manjaro-arm-installer)

```bash
git clone https://gitlab.manjaro.org/manjaro-arm/applications/manjaro-arm-installer
cd manjaro-arm-installer
chmod +x manjaro-arm-installer
sudo bash ./manjaro-arm-installer arm-unstable
```
## 切换Unstable分支与更新

[Manjaro Forum](https://forum.manjaro.org/t/vlc-has-a-display-error/175412/6)

```bash
sudo pacman-mirrors -aS unstable && sudo pacman -Syyu
```

## 安装输入法

```bash
sudo pacman -S fcitx5 fcitx5-configtool fcitx5-qt fcitx5-gtk fcitx5-chinese-addons
```

前往`设置`>`键盘`>`虚拟键盘`选择`Fcitx5`

## 自动关机防熄灯

安装`KAlarm`，创建模板以新建闹钟（空模板就行）。

设置显示闹钟以设置提醒，设置命令闹钟以自动关机。

## Yay

安装`fakeroot`等打包工具。

```bash
sudo pacman -S base-devel
```
