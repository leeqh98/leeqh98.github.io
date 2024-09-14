---
title: Build Hexo Blog
tags: 
  - Hexo
  - nodejs
  - git
categories: 
  - Hexo 博客
---

# 构建 hexo 静态博客

## 准备环境 安装

* git 版本控制工具(可选) 配合 GitHub 使用
* nodejs hexo 是 nodejs 的一个包
* hexo-cli 博客构建工具
* hexo-theme-next 博客主题
* typora 写 markdown 的编辑器(付费), 也可以使用 vscode 或者其他的编辑器

1. 安装 nodejs

[Node.js — Jalankan JavaScript Di Mana Saja (nodejs.org)](https://nodejs.org/id)

nodejs 网站安装 nodejs lts 长期支持版本,或者使用 winget 安装

```powershell
winget install Schniz.fnm
```

另外一个安装方式是使用 nvm node 的版本控制工具.

验证安装的 nodejs 是否成功. 在 终端(terminal)中运行

``` powershell
node -v
npm -v
```



2.  安装 hexo-cli

由于一些网络原因, 先修改包的安装源. 将包源替换为淘宝软件源.



``` powershell
npm config set registry https://registry.npmmirror.com
```

[Hexo](https://hexo.io/zh-cn/) 博客框架的网站

``` powershell
npm install hexo-cli -g # 全局安装 hexo工具
hexo init blog # 新建博客项目 blog(项目名)
cd blog
npm install
hexo server
```



这里可以按照 [GitHub Pages](https://pages.github.com/) 上的流程创建一个项目

```powershell
hexo init user.github.io # user 修改为你自己的用户名
```

然后在这里创建 ``git init -b main `` 仓库,然后在本地仓库中添加文件, 提交暂存文件.

```powershell
git add .
git commit -m "First commit"
git remote add origin REMOTE-URL
git remote -v
git push origin main
```



1. [将本地托管代码添加到 GitHub - GitHub 文档](https://docs.github.com/zh/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github)






3.  安装 hexo-theme-next

1. [NexT - Theme for Hexo (theme-next.js.org)](https://theme-next.js.org/)

2. [hexo-theme-next/docs/zh-CN/README.md at master · next-theme/hexo-theme-next (github.com)](https://github.com/next-theme/hexo-theme-next/blob/master/docs/zh-CN/README.md)

   ``` powershell
   cd hexo-site
   npm install hexo-theme-next		
   ```

   然后在 _config.yml 中将 theme 改为 next.

[Configuration | NexT (theme-next.js.org)](https://theme-next.js.org/docs/getting-started/configuration.html)

进一步的配置

```
hexo clean
hexo server
```






3. 






##  配置 

1. hexo



2. hexo-theme-next

四种模式

* Gemini 双子



* mist 朝雾



* Muse 缪斯



* Pisces 双鱼	





3. 部署 GitHub action

在根目录创建 ``.github\workflow\github-action-deploy.yml `` 文件,用来部署 GitHub action. 

```
name: Hexo Deploy Github Pages
on:
  push:
    branches:
      - master
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v1
    - name: Build and Deploy
      uses: renzhaosy/hexo-deploy-action@master
      env:
        PERSONAL_TOKEN: ${{ secrets.ACCESS_TOKEN }} # github 私人权限token
        PUBLISH_REPOSITORY: renzhaosy/renzhaosy.github.io # 打包之后想要部署到的仓库
        BRANCH: master # 打包之后想要部署到的分支
        PUBLISH_DIR: ./public  # hexo 打包之后文件的所在的文件夹


        # https://renzhaosy.github.io/2019/11/09/github-action/ 参考网站
```





[Custom Pages | NexT (theme-next.js.org)](https://theme-next.js.org/docs/theme-settings/custom-pages)

[开始使用 - NexT 使用文档 (iissnan.com)](https://theme-next.iissnan.com/getting-started.html)

参考链接,进行进一步的各类设置.

* 头像
* 多页面
  * Home
  * tag
  * archives
  * categories
  * series
  * notes
  * about

* cc 协议设置

## 写博客

``` 
hexo new "My New Post" # 写博文
hexo server # 运行服务器
hexo generate # 生成静态文件
hexo deploy # 部署站点
hexo list [type] # post page route tag category


hexo new [layout] <title> # 布局有三种 post page draft
```

在文件开头添加上 yaml front-matter,
标签和目录区分开来,相当于是分类和标签, 注意 开头的格式要注意缩进.