---
title: mac系统下的Maven安装配置
permalink: Maven_primary_knowledge
date: 2018-12-25 13:35:58
categories: maven
tags: [maven, java, mac]
---

# **Maven的安装**
前往<a href="https://maven.apache.org/download.cgi" rel="external" >Apache Maven官网</a>，找到<code>Files</code>下面的<code>apache-maven-x.x.x-bin.tar.gz</code>。点击<code>apache-maven-x.x.x-bin.tar.gz</code>链接下载即可。下载后解压下载的安装包到某一目录，比如：/Users/xxx/Documents/maven。这样我们便成功安装好maven管理工具，但这还不够，还需要设置maven环境变量。
<!--more-->
# **配置Maven环境变量**
打开终端，根目录，输入命令:<code>$ vi ~/.bash_profile</code>打开bash_profile文件,然后添加如下两行代码:

```
export M2_HOME=/Users/xxx/Documents/maven
export PATH=$PATH:$M2_HOME/bin
```
然后继续退回到根目录，输入<code>$ source ~/.bash_profile</code>使bash_profile文件添加的内容即刻生效。
接下来在终端输入<code>mvn -v</code>,来测试是否安装成功。
