---
layout: post
title: "AS新打开工程Gradle下载慢问题fix"
date: 2017-04-22 18:01:00 +0800
comments: true
categories: 
---

#### 打开新工程，下载Gradle慢问题fix
1. 切到目录.gradle/wrapper/dists/，查看当前在下载的版本；  
2. 搜索对应Gradle版本下载；  
    > 参考链接：http://www.androiddevtools.cn/  
    > 不推荐Gradle官网，慢  
3. 切到目录.gradle/wrapper/dists/版本XX/XXXX，删除对应版本XX.part文件；  
4. 拷贝下载的对应版本Gradle文件至目录.gradle/wrapper/dists/版本XX/XXXX；  
5. 重启AS；  

<!--more-->

#### 构建新工程，下载依赖包慢问题fix
1. 修改项目根build.gradle配置文件，引入阿里云私服；  
```groovy
buildscript {
    repositories {
        maven {
            url 'http://maven.aliyun.com/nexus/content/groups/public/‘
        }
    }
}

allprojects {
    repositories {
        maven {
            url 'http://maven.aliyun.com/nexus/content/groups/public/‘
        }
    }
}
```