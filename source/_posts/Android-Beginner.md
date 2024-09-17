---
title: Android Beginner
date: 2024-09-17 22:11:00
tags: gradle
categories:
---

# android 的初始配置

``` powershell
└── MyApp/  # Project
    ├── gradle/
    │   └── wrapper/
    │       └── gradle-wrapper.properties # 这是 gradle的配置文件 在这里设置国内镜像
    ├── build.gradle(.kts)  # 这里配置maven的镜像源
    ├── settings.gradle(.kts)
    └── app/  # Module
    │   ├── build.gradle(.kts)
    │   ├── build/
    │   ├── libs/
    │   └── src/
    │        └── main/  # Source set
    │            ├── java/
    │            │   └── com.example.myapp
    │            ├── res/
    │            │   ├── drawable/
    │            │   ├── values/
    │            │   └── ...
    │            └── AndroidManifest.xml
```

gradle.properties

这个文件是另一个配置文件

一共要 配置 gradle 和 maven的镜像

分别是

gradle-wrapper.properties

build.gradle(.kts)
