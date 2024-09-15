---
title: computer science notes 001
date: 2024-09-15 22:02:03
tags: notes
categories:计算机科学笔记
---

# 计算机科学笔记 001

[toc]

计算机科学发展起来的很多概念, 来自于硬件,但是随着时代的发展,很多东西就消失了,后来人理解起来就比较困难,这也是一些人说的,想要了解一门学科,就去看历史上他们面临的各种问题.然后你会理解很多理论的来源.

比方说 图标,窗口,缓存,鼠标,键盘,指针,光标,滑动条.输入法,字体,菜单,这些东西在早期的Windows 系统里 xp 95 win7 都有说明书之类的东西介绍.所以想要成为数量用户或者超级用户也是挺困难的.而且现在的手机和电脑的操作逻辑也是不一样.

另外这上边也是一些设计模式的体现,安全仓模式,用户界面的风格等等.



## 终端 shell 控制台 电传打字机

很多的概念来源的实体消失了,所以就理解不容易.就像传真,电话亭等等已经快消失了.软盘,磁带等等.还有一些别的东西,可能不是很普及.

### terminal

早期是物理硬件设备,



### shell





### console





### teletype

电传打字机也是一个硬件设备曾经.没有显示屏,键盘输入之后,输出是到纸上面.也是一种终端.

### 参考链接

1. [What is the difference between shell, console, and terminal? - Super User](https://superuser.com/questions/144666/what-is-the-difference-between-shell-console-and-terminal)
2. [控制台、终端和 shell 之间有什么区别？- Scott Hanselman 的博客](https://www.hanselman.com/blog/whats-the-difference-between-a-console-a-terminal-and-a-shell)



## 文件夹和目录

directory folder list index

gui 图形界面下称呼为文件夹,在命令行中是 目录; ``ls; dir``

pwd 是print working directory;

Windows 中的库,下属多个文件夹,实际上没有这个目录,下面都是别的地方的目录.

一个文件系统的概念,一个是用户界面的产物.

为什么在 Linux 中的文件夹被称为目录？ - 醉卧沙场的回答 - 知乎
https://www.zhihu.com/question/562082254/answer/2748737538





## 具体的使用

Linux 的文件层次结构系统 lfhs 这个标准中对各个目录需要存放那些文件都有规范,只是有些历史遗留问题, unix 老系统了,好像还有 lsb posix 这两个规范

Windows 的文件系统也是对安装位置有所规范, 各种默认的安装位置,配置文件的存放,还有注册表等等.



用户下的个人用户 ;公用;default 都是干什么用的,另外像多用户系统,感觉自己都没怎么建立过多个账号.





programanddocument; program files(x86); program files; appdata; 

appdata: local; locallow; roaming;

有的配置选项是 xp 系统的产物,或者 8.3 格式的时候产物.兼容性强的原因.

爱奇艺,迅雷之类的软件垃圾文件到处扔,公用账号下也是各种垃圾.



Windows 的[库] 机制,让用户不用关心具体的路径之类的问题,现在的手机也是如此,一般人根本不用关心文件存放的位置, 只要用户层面点点点.

Windows 的很多功能缺乏使用场景,或者自己完全不会用.一些自带的系统管理工具.家庭组和局域网共享功能没有用过,远程桌面功能也是很少使用.组策略
