---
title: VScode配置C/C++环境
date: 2021-11-04
collapsable: true
cover: /img/slm.jpg
tags:
 - VScode
 - C/C++
categories: 
 - Tip
---

众所周知，VScode是万能的
<br>就是麻烦了点点!!
<!-- more -->

# VScode配置C/C++环境
Windows操作系统下VScode配置C/C++环境
## 前置知识
再次之前你需要了解
- VScode安装
- Windows环境变量
- Windows系统文件管理系统

:::tip
VScode官方下载会很慢，这里我建议用[镜像源下载](https://update.code.visualstudio.com/latest/win32-x64-user/stable)
:::

## VScode扩展
所需的扩展有`C/C++`与`C/C++ Runner`
<br>按 shift+ctrl+x 打开 VScode 扩展列表界面
<br>在搜索栏搜索以上扩展即可

## Mingw下载
我们这里用编译好的.zip压缩包，解压后即可用
<br>点击下载[Mingw-x86_64](https://zfile.yin0mc.ltd/s/b7dwiq)
<br>当然也可以去Mingw官网（不建议，以为太慢了）
<br>下载好后解压到自己记得的位置

## gcc环境变量配置

