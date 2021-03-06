﻿---
layout: post
title: Git命令使用（GitHub篇）
date: 2019-03-09 
tag: Git
---

###  1. 将项目从GitHub克隆到本地：git clone

![](/images/posts/Git/Git1.png)

问题1：当该路径下已经存在与repository同名的文件夹，则会出现如下错误：

![](/images/posts/Git/Git2.png)

解决方法：到该路径下删除或重命名同名文件夹

问题2：执行目录错误，执行目录一定要切换到根目录~

![](/images/posts/Git/Git3.png)

解决方法：切换到根目录  cd~

区别：git clone和git pull

git clone:适用于本地没有repository的情况，将整个repository从GitHub下载下来

git pull:适用于本地有repository的情况，将repository 里更新后数据下载过来，并且与本地代码merge
 
### 2. 进入要push的目标文件夹，右击，打开Git Bash

![](/images/posts/Git/Git4.png)

### 3. 初始化：git init

init后会出现.git隐藏文件夹—本地代码库

![](/images/posts/Git/Git5.png)

### 4. 加载文件：git add .(注意：先空格再键入点.)

![](/images/posts/Git/Git6.png)

### 5. 提交文件，创建时间点：git commit -m “时间点”

![](/images/posts/Git/Git7.png)

### 6. 查看状态：git status

![](/images/posts/Git/Git8.png)

### 7. 推送代码

第一次推送，添加远程的代码库到配置：git remote add origin https://github.com/your repositoryname

![](/images/posts/Git/Git9.png)

问题：如果之前添加过配置，则会出现问题

![](/images/posts/Git/Git10.png)

解决方法：无需添加配置，推送代码即可

推送代码：git push origin master

![](/images/posts/Git/Git11.png)

问题：如果GitHub上repository比本地代码库的代码新，则会出现问题

![](/images/posts/Git/Git12.png)

解决方法：将GitHub上的代码pull下来，在本地修改，再将修改后的代码push到GitHub上

![](/images/posts/Git/Git13.png)

强制推送：git push -f origin master

![](/images/posts/Git/Git14.png)

### 参考资料：

Git 中 pull 和 clone 的区别
https://blog.csdn.net/HeatDeath/article/details/79135462

Git之Github使用（一）：Push代码到Github
http://www.cnblogs.com/android-blogs/p/5816833.html

转载请注明：[孙仲锴的博客](https://sunzhongkai0110.github.io) » [Git命令使用(GitHub篇)](https://sunzhongkai0110.github.io/2019/03/2019/03/Git命令使用-GitHub篇/)

