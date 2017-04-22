---
layout: post
title: "Mac终端iTerm2 Solarized主题配置"
date: 2017-04-22 17:34:08 +0800
comments: true
categories: Mac
---

#### 配色方案下载
1. Solarized仓库；  
> https://github.com/altercation/solarized

#### 设置配色方案
1. 进入目录solarized/iterm2-colors-solarized，双击Solarized Dark.itermcolors、Solarized Light.itermcolors导入主题；  
2. iTerm2设置->Profiles->Colors->Color Presets…;  
![item2主题配置](../images/mac_iterm2/iterm2_theme_config.jpeg)

#### 设置VIM配色
1. 进入目录solarized/vim-colors-solarized/colors，拷贝solarized.vim到目录~/.vim/colors；  
2. 配置vim.rc；  
```
syntax enable
set background=dark
colorscheme solarized
```

#### 设置ls配色
1. ~/.bash_profile配置；  
```
export CLICOLOR=1
```
