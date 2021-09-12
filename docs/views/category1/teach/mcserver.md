---
title: 用自己的win10电脑搭建本地mc服务器
date: 2021-08-20
cover: https://file.yin0mc.ltd:100/images/yourname.jpg
tags:
 - mc
categories:
 - 教程
---

:::tip
感觉别人的服务器好好玩，也想在自己电脑上搭一个？  
现在我们来看一下，  
怎么在自己的win10电脑上搭建一个本地的mc服务器
:::
<!-- more -->  

# 前提条件  
*需要java  
**[java8](https://www.oracle.com/java/technologies/javase-jre8-downloads.html)  
**[java16](https://www.oracle.com/java/technologies/javase-jdk16-downloads.html)  
*需要能稳定运行的win10  
**[baidu](https://www.baidu.com)  
*需要脑子(bushi)  
:::warning
mc游戏版本1.16以下使用java8,1.16及以上请使用java16  
:::

## 服务端下载  
这里我们以paper-1.14.4为例  
[papermc](https://papermc.io/)  
![mc1](https://file.yin0mc.ltd:100/curse/imgs/mc1.png)  
首先我们找到网页右上角的`DOWNLOADS`字样,然后点击它  
![mc2](https://file.yin0mc.ltd:100/curse/imgs/mc2.png)  
再找到1.14.4，点击下面的`DOWNLOAD ANYWAY`  
![mc3](https://file.yin0mc.ltd:100/curse/imgs/mc3.png)  
等待下载完成........  
这里我们点`保留`  
![mc4](https://file.yin0mc.ltd:100/curse/imgs/mc4.png)  
打开下载文件夹，我们会发现陆陆续续的出现5个东西  
![mc5](https://file.yin0mc.ltd:100/curse/imgs/mc5.png)  
然后我们把这5个东西剪切到别的文件夹，因为这样好找，也好管理  
如果没有出现5个东西，只有一个paper-1.14.4也没关系的，一样的操作  
将paper1.14.4剪切到别的文件夹  

## 启动文件  
接下来我们写启动文件  
首先我们在与`paper-1.14.4-xxx`同目录下`右键`-`新建(w)`-`文本文档`  
将起命名为start.bat  
:::tip
如果你看不到后缀名，请在资源管理器（此电脑）上方找到"查看"然后勾上文件扩展名  
:::  
然后选择`start.bat`-`右键`-`编辑`  
在里面填入  
```sh
java -Xms512M -Xmx4G -jar paper-1.14.4-243.jar
```  
然后ctrl+s保存，叉掉  

## 解读.bat文件  
### java  
这个参数指用java启动  
参数可以改为java安装路径，如  
```
"C:\Program Files\Java\jre1.8.0_291\bin\java.exe" -Xms512M -Xmx4G -jar paper-1.14.4-243.jar
```  

### Xms  
指设置最小java虚拟内存，后面接容量，如-Xms512M就是最小分配512MB内存给我们的服务器  

### Xmx  
指设置最大java虚拟内存，后面接容量，如-Xms4G就是最大分配4GB内存给我们的服务器  
:::tip
不同电脑性能不同，自己酌情更改  
:::  

### jar  
指启动文件后缀为.jar 后面接文件名，如-jar paper-1.14.4-243.jar  
:::tip
不同可能你们下载过来的不是paper-1.14.4-243.jar,根据你们下载的paper-1.14.4-xxx.jar更改  
:::  

## 开启服务器  
双击start.bat就能开启服务器了  
然后你会突然闪退什么的，是因为我们的eula.txt里面的协议没有同意  
:::tip
之前提到下载paper-1.14.4-xxx.jar时不会给我们下载5个东西，只有一个paper-1.14.4-xxx.jar的情况  
在双击start.bat的时候会自动下载，所以，只有paper-1.14.4-xxx.jar也不用担心  
:::  
然后我们双击eula.txt,将末尾的`eula=false`的`false`改为`true`,再按ctrl+s保存，叉掉  
我们再次点击`start.bat`就能顺利开启服务器啦!!!  
当我们的控制台出现`Timings Reset`就说明我们的服务器已经成功开启啦~  

## 服务器加入  
服务器已经开启了，那么我们要怎么加入我们的本地服务器呢？  
打开我们的Minecraft1.14.4  
然后点击多人游戏  
再点击添加服务器  
输入ip: `127.0.0.1` 或 `localhost`  
然后会出现一个信号满格的服务器  
双击加入就行啦  

## 服务器操作
### 给自己op  
你只需要在刚刚开启的服务器控制台输入  
`op <你自己的游戏id>`就可以啦！  
:::tip
控制台输指令不用输'/'哦
:::

### 加入插件  
将自己从别的地方下载过来的xxx.jar插件拖入`plugins`文件夹  
然后在服务器控制台输入`stop`,等待控制台关闭后，再双击`start.bat`文件,等待服务器启动就好了~

### 邀请好友加入  
这里你需要知道怎么内网穿透  
请自行百度“内网穿透”  
ip为127.0.0.1  
端口为25565  
端口映射出去后，让好友使用映射的ip链接即可  
:::warning
当你的电脑关闭后，你的好友也会失联哦  
:::  

如有问题，请在评论区留言，看到会第一时间回复哦~  