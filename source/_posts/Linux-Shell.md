---
title: Linux Shell
date: 2024-09-16 09:23:43
tags: Shell, Bash, Zsh
categories: Linux 教程
---
# Linux Shell

linux shell 默认的一般是 bash，旧版的sh 像 bushbox 配的sh，如果有条件直接用fish 使用起来自动补全，默认配置都可以了。如果想用zsh，然后就再安装oh-my-zsh 配上 nerd font 感觉配置起来也麻烦，最好的永远是开箱即用的工具，这样不会依赖特定的电脑。

## oh-my-zsh 配置使用
[oh-my-zsh](https://ohmyz.sh/)
我好像安装错软件了。

[oh-my-posh](https://ohmyposh.dev/docs/installation/fonts#) 


```bash
curl -s https://ohmyposh.dev/install.sh | bash -s # 安装oh-my-posh
export PATH=~/.local/bin:$PATH
oh-my-posh font install 

```

## 基本的linux 命令
info bash 学习一遍bash 的手册，然后在随用随查。
man info help appros tldr
which type file whoami 
cd pwd ls ll clear mv rm cp cat tar head tail less more 
cd ~; cd ..; cd -;

