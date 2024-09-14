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

<img src="./../../../../../AppData/Roaming/Typora/typora-user-images/image-20240914211509613.png" alt="image-20240914211509613" style="zoom:33%;" />

* mist 朝雾

<img src="./../../../../../AppData/Roaming/Typora/typora-user-images/image-20240914211728491.png" alt="image-20240914211728491" style="zoom:33%;" />

* Muse 缪斯

<img src="./../../../../../AppData/Roaming/Typora/typora-user-images/image-20240914212014950.png" alt="image-20240914212014950" style="zoom:33%;" />

* Pisces 双鱼	

<img src="./../../../../../AppData/Roaming/Typora/typora-user-images/image-20240914211914532.png" alt="image-20240914211914532" style="zoom:33%;" />







## 写博客

``` 
hexo new "My New Post" # 写博文
hexo server # 运行服务器
hexo generate # 生成静态文件
hexo deploy # 部署站点

```

