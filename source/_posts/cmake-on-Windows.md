---
title: cmake on Windows
date: 2024-11-30 11:43:37
tags: CMake
categories:
---

# 在windows 上使用 cmake

1. 安装

   cmake 官网上下载安装软件。

2. 配置

   在program 目录下，创建 ``CMakeLists.txt`` 文件，其中添加配置内容

   ```cmake
   # version setting
   cmake_minimum_required(VERSION 3.30)
   
   # project name and version 
   project(program VERSION 0.0.1)
   
   # add execute name
   add_executable(program program.c)
   
   
   ```

   

3. 构建

​	pwd: path\to\project;

````powershell
mkdir build
cd build
cmake ..
````

4. 运行

   ```powershell
   cmake --build . --config Release
   
   .\Release\program.exe
   ```

   

5. 清理构建

   ```powershell
   cmake --build . --target clean
   ```

   
