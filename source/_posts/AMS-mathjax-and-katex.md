---
title: AMS mathjax and katex
date: 2024-09-18 00:30:58
tags: 
  - mathjax
  - katex
categories: 数学公式
katex: true
---

# 数学公式

[toc]

数学公式的复杂排版一个是靠 latex, 网页上 就是 mathjax 或者 katex ,在 飞书和语雀中都有一些语法支持,此外 这是 markdown 也有typora 这个本地的工具可以边写边看,不行就做出图片插入进来.还有typst 可以做排版.

考虑在弄弄 mindmap 之类的支持的markdown 插件.

飞书支持的katex, 语雀的也是 katex

katex 速度快,支持的公式不全面,mathjax 支持的多,但渲染速度慢(不知道是不是还是这样)

[hexo-theme-next/docs/zh-CN/MATH.md at master · theme-next/hexo-theme-next (github.com)](https://github.com/theme-next/hexo-theme-next/blob/master/docs/zh-CN/MATH.md)

配置参考

```
npm un hexo-renderer-marked
npm i hexo-renderer-markdown-it-plus

```

#### 已知的问题



1. 首先请查阅 Katex 的 [Common Issue](https://github.com/Khan/KaTeX#common-issues)
2. 块级公式(例如 `$$...$$`)必须位于空行。
   即在开头的 `$$` 前和在结尾的 `$$` 后不能有除了空白字符以外的其他字符。([#32comment](https://github.com/theme-next/hexo-theme-next/pull/32#issuecomment-357489509))
3. 不支持 Unicode。([#32comment](https://github.com/theme-next/hexo-theme-next/pull/32#issuecomment-357489509))
4. 行内公式(例如 `$...$`)在开头的 `$` 后面和结尾的 `$` 前面**不能含有空格**。([#32comment](https://github.com/theme-next/hexo-theme-next/pull/32#issuecomment-357489509))
5. 如果你在文章的各级标题中(例如 `## 标题`)使用公式。
   那么文章目录中的这个标题会出现 3 次未渲染的公式代码([#32comment](https://github.com/theme-next/hexo-theme-next/pull/32#issuecomment-359018694))
6. 如果你在文章 Title 中使用公式，那么公式将不会被渲染。([#32comment](https://github.com/theme-next/hexo-theme-next/pull/32#issuecomment-359142879))



各种符号,字体等等.

## 例子

#### 矩阵和数组

$\begin{matrix} a & b \\ c& d \end{matrix}$

$\begin{Vmatrix}1&2\\3&4\\ \end{Vmatrix}$

$\begin{pmatrix}
 1 & a_1 & a_1^2 & \cdots & a_1^n \\
 1 & a_2 & a_2^2 & \cdots & a_2^n \\
 \vdots  & \vdots& \vdots & \ddots & \vdots \\
 1 & a_m & a_m^2 & \cdots & a_m^n    
 \end{pmatrix}$

$\begin{CD} A @>a>>B \\ @VbVV @AAcA \\ C @= D \end{CD}$

$\begin{array}{c|lcr}
n & \text{Left} & \text{Center} & \text{Right} \\
\hline
1 & 0.24 & 1 & 125 \\
2 & -1 & 189 & -8 \\
3 & -20 & 2000 & 1+10i
\end{array}$

#### 方程组

$\left\{ 
\begin{array}{c}
a_1x+b_1y+c_1z=d_1 \\ 
a_2x+b_2y+c_2z=d_2 \\ 
a_3x+b_3y+c_3z=d_3
\end{array}
\right.$

#### 其他

$\sum_{n=1}^\infty \frac{1}{n^2} \to
  \textstyle \sum_{n=1}^\infty \frac{1}{n^2} \to
  \displaystyle \sum_{n=1}^\infty \frac{1}{n^2}$





----

[文档支持的公式 (feishu.cn)](https://www.feishu.cn/hc/zh-CN/articles/014150532397-文档支持的公式)

[数学公式举例 (yuque.com)](https://www.yuque.com/yuque/gpvawt/brzicb)

[Supported Functions · KaTeX](https://katex.org/docs/supported.html)
