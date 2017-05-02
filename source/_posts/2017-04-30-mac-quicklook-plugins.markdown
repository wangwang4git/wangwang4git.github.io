---
layout: post
title: "Mac QuickLook Plugin推荐"
date: 2017-04-30 23:55:30 +0800
comments: true
categories: 
---

QuickLook功能异常强大，一个空格键，即可以预览众多格式文件，比如pdf、图片等。  
但是也有一些文件没法预览，比如`md`文件，即MarkDown文档。  
那么有没有办法扩充预览的能力呢？答案就是安装插件！  
比如MarkDown文件预览就有一个`QLMarkdown`插件，[github链接](https://github.com/toland/qlmarkdown)。  

安装QuickLook有两种方法，分别介绍如下：  

#### 自动安装
使用`brew cask`安装卸载软件，如果你还不知道brew、cask请自行Google。  

###### 1. 安装  
```sh
brew cask install <pluginname>  
```

###### 2. 卸载  
```sh
brew cask uninsatll <pluginname>  
```

#### 手动安装
如果不能通过cask安装卸载，可以采用手动方式安装卸载。  

###### 1. 卸载对应插件的二进制包，一般可以从github仓库找到下载链接，解压获取.qlgenerator插件文件；  
###### 2. 将插件文件copy到~/Library/quicklook文件夹，如果没有quicklook文件夹自己创建一个；  
###### 3. 在终端执行如下命令生效  
```sh
qlmanage -r  
```
###### 4. 如果要卸载对应插件，直接在~/Library/quicklook文件夹删除对应.qlgenerator文件即可；  

#### 插件推荐
讲完了如何安装插件，那有哪一些插件值得推荐呢，可以参考这个网站[QuickLook Plugins List](http://www.quicklookplugins.com/)，里面有相当多的插件，可以按自己需要安装喜欢的插件。  

<!--more-->

这里推荐一些开发会用到的插件：  
###### 1. QLMarkdown  
https://github.com/toland/qlmarkdown  
预览MarkDown文件  
###### 2. QuicklookStephen  
https://github.com/whomwah/qlstephen  
预览无文件扩展名的文本文件，比如开发常用到的如下文本文件，支持预览的感觉特别赞  
```
README  
INSTALL  
Capfile  
CHANGELOG  
.gitignore  
...
```
###### 3. qlImageSize  
https://github.com/Nyx0uf/qlImageSize  
在预览窗口title bar上展示图片尺寸与大小，并且对于Web、bpg支持预览，在Finder中也会展示图片尺寸，也能预览  
这个插件强烈推荐，效果如下：  

{% img center /images/quicklook/qlImageSize01.png 预览窗口title bar效果 %}  

{% img center /images/quicklook/qlImageSize02.png Finder效果 %}  

#### 参考链接
1. [那些强大的「预览」插件](https://medium.com/@Chenz5dong/%E9%82%A3%E4%BA%9B%E5%BC%BA%E5%A4%A7%E7%9A%84-%E9%A2%84%E8%A7%88-%E6%8F%92%E4%BB%B6-mac-5d9b6f31efdd)