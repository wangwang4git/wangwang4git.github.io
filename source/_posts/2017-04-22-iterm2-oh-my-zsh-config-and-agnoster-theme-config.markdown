---
layout: post
title: "iTerm2 oh-my-zsh配置与agnoster主题配置"
date: 2017-04-22 18:47:39 +0800
comments: true
categories: Mac
---

先上一张效果图  

{% img center /images/mac_iterm2/iterm2_effect.jpeg iTerm2配置效果图 %}  

#### 配置过程如下

###### 1. 下载iTerm2  
> 链接：http://www.iterm2.com/  

###### 2. 下载oh-my-zsh  
> 链接：https://github.com/robbyrussell/oh-my-zsh  
> 查看当前终端是否已经启动zsh，命令`echo $0`，如果不是zsh使用命令`chsh -s /bin/zsh`修改  
> 查看系统支持的sh环境，命令`cat /etc/shell`  

###### 3. 安装Powerline对应的字体库  
> Powerline链接：http://powerline.readthedocs.io/en/master/  
> 为了展示agnoster主题提示符里的三角形，需要Powerline字体库的支持  
> 使用pip安装，安装命令`pip install powerline-status`；如果没有pip，请先安装pip，安装pip命令`sudo easy_install pip`  
> 字体库链接：https://github.com/powerline/fonts  
> 使用git clone下来字体库仓库，进入仓库根目录，执行`install.sh`安装  

###### 4. 设置iTerm2字体  
> 进入iTerm2设置-Profiles-Text-Font，选择Powerline字体`12pt Meslo LG S DZ Regular for Powerline`  

{% img center /images/mac_iterm2/iterm2_font_config.jpeg iTerm2字体设置 %}  
<!--more-->

###### 5. 安装Solarized配色方案  
> 参考前文[Mac终端iTerm2 Solarized主题配置](http://wangwang4git.github.io/blog/2017/04/22/mac-iterm2-solarized-theme-config/)  

###### 6. 使用agnoster主题  
> 链接：https://github.com/fcamblor/oh-my-zsh-agnoster-fcamblor  
> git clone，进入仓库根目录，执行install文件  
> 配置iTerm2主题，打开~/.zshrc，设置ZSH_THEME="angoster"  

#### 附加项
###### 7. 增加指令高亮效果/zsh-syntax-highlighting  
> 用户输入错误指令为红色，输入正确指令为绿色  
> zsh-syntax-highlighting链接：https://github.com/zsh-users/zsh-syntax-highlighting  
> git clone到XX目录，打开.zshrc文件添加
```sh
source XXX/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh  
plugins=(zsh-syntax-highlighting)
```

指令高亮效果图如下：  
{% img center /images/mac_iterm2/iterm2_right.jpeg 指令正确 %}  
{% img center /images/mac_iterm2/iterm2_error.jpeg 指令错误 %}  

#### 参考文献
1. [iTerm 2 && Oh My Zsh【DIY教程——亲身体验过程】](http://www.jianshu.com/p/7de00c73a2bb)