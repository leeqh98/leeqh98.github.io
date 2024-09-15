---
title: Git beginner
date: 2024-09-15 21:14:04
tags: Git
categories: Git教程
---

# Git 教程

[toc]

## 概念

仓库; 分支; 本地仓库; 远程仓库; 提交; 拉取; 推送; 工作目录; 暂存区; 标签; head 指针; 合并; 

repository; branch; local repository; remote repository; commit; pull; push; work directory; cache; tag; head pointer; merge

vcs(version control system); scm(source code management )

从版本控制的需求出发,理解这种工具背后的思想方法.

去中心化的版本控制系统, 只要想要控制版本,多人协作.就需要查看不同版本,掌握进度, 合并版本.

工具有 subversion (svn) cvs mercurial(hg) git

```bash

These are common Git commands used in various situations:

start a working area (see also: git help tutorial) 准备工作
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday) 日常
   add       Add file contents to the index
   mv        Move or rename a file, a directory, or a symlink
   restore   Restore working tree files
   rm        Remove files from the working tree and from the index

examine the history and state (see also: git help revisions) 修正 
   bisect    Use binary search to find the commit that introduced a bug
   diff      Show changes between commits, commit and working tree, etc
   grep      Print lines matching a pattern
   log       Show commit logs 日志
   show      Show various types of objects
   status    Show the working tree status 状态

grow, mark and tweak your common history
   branch    List, create, or delete branches
   commit    Record changes to the repository
   merge     Join two or more development histories together
   rebase    Reapply commits on top of another base tip
   reset     Reset current HEAD to the specified state
   switch    Switch branches
   tag       Create, list, delete or verify a tag object signed with GPG

collaborate 协作 (see also: git help workflows) 工作流
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects
```



### 常用的命令

> init; clone; add; commit; pull; push; fetch; branch; checkout; config; log; status; remote; 



### 代码托管平台

git 是协作工具,代码托管平台;

#### 国外

* bitbucket
* GitHub
* gitlab

#### 国内

* coding
* 码云 gitee
* gitcode
* 

### 参考文献和教程

#### 自带的

```bash
git help
git help --guide
* core-tutorial
* everyday
* faq
* glossary
* tutorial
* tutorial-2
workflows
* remote-helpers
git help git

```



#### 网站

廖雪峰 的班组

pro-git 中文手册

GitHub 上的帮助文档,



网络上随便搜索都有教程.码云的帮助页面一堆,但是质量良莠不齐.

在学习这个工具之前,其实可以先从需求来思考,本身git 的很多操作方式只是自己的一套体系,当明白这些操作的目的是干什么的,就更容易把握.整体来看待.

创建一个项目; 然后开始工作; 一个人的话可能多台设备,需要进行进度协作. 一个人一台设备.只是考虑的备份和新旧版本的查看.不行就自己手工管理.需要每次版本更新留档记录. 两人或两台设备以上就需要考虑冲突问题. 远程仓库就是一个主要仓库,其实感觉上是两个分布式的仓库,同时都有工作进行.然后一个仓库算是远程的,用来备份的.然后两边各自开展还好,如果有同一个文件进行了修改,那就会发生冲突.或者两边的工作没法合并了.需要你时刻和远程仓库更新,两个仓库合并.

图像化的工具值了的

git; tortoise git; visual studio code 插件 git history gitgraph ; git kraken;



## 配置

```
git config --list # 查看已有配置
git config --global #
git config --global user.name "username"
git config --global user.email "email address"
```

关于 ``.gitignore ``文件的配置

``GitHub``  的配置文件夹 ``.github`` 里边有关于 workflow 工作流的配置

vscode 的配置文件夹 中有关于 task.json run.json. 等等.

另外配置文件一般是json,toml.等等.yml也可以.

和GitHub 进行密钥绑定等等.这个工作看GitHub 文档 ssh 链接.网络可能不太好.

coding或者码云试试

## 创建仓库

``` bash
git init 
git add . # 添加全部文件到暂存区
git commit # 提交
git diff --cached # 查看提交内容
git status # 查看状态
git log # 查看日志
```





```bash
git log -p # 查看内容
git log --stat --summary # 查看总结
```



## 创建分支



``` bash
git branch [branch name] # 新建分支
git checkout [branch name] # 切换到该分支
git checkout -b [branch name] # 切换到该分支并直接工作
git branch # 查看所有分支
git switch main # 切换分支 main/master 的区别
git merge [branch name] # 合并分支
git diff # 查看冲突
git merge [branch name] # 合并分支
git diff # 查看冲突的内容
gitk # 查看提交
```



在不同分支进行不同的工作,然后合并分支,git tag version 标记版本.

## 协作

可以考虑两台电脑自己体验这个协作的流程

主分支 main 远程仓库

thinkbook: leeqh98 用户

thinkpad: liqh98 用户

在GitHub上使用时,可以考虑使用 gh 工具来完成,然后将这些都图形界面和命令行界面同时进行.



##  推送

```bash
git remote -v
git pull 
git push -u origin main

```







## 日常

git add file

git commit -m "commit message"

[git tag version]

git push -u origin main

