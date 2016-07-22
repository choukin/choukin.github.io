---
layout: post
title: Git同一台电脑多个git账号
description: "Git.多账号"
modified: 2016-04-29
tags: [git]
image:
  feature: avatar.jpg
  credit: dargadgetz
  creditlink: http://www.dargadgetz.com/ios-7-abstract-wallpaper-pack-for-iphone-5-and-ipod-touch-retina/
---

## Git命令
###生成新账号的公钥和私钥
1.用ssh-keygen命令生成一组新的id_rsa_new和id_rsa_new.pub。
> ssh-keygen -t rsa -C "your new email"

不要直接回车，直接回车默认生成id_rsa和id_rsa.pub。这里特别需要注意，出现提示输入文件名的时候要输入与默认配置不一样的文件名，比如：  id_rsa_new。

执行ssh-agent让ssh识别新的私钥
>ssh-add ~/.ssh/id_rsa_new



2.配置~/.ssh/config文件
> 
# 加上以下内容
#default github
Host 192.168.45.120
  HostName 192.168.45.120
  IdentityFile ~/.ssh/id_rsa

Host github_zhaoxin
  HostName github.com
  IdentityFile ~/.ssh/id_rsa_zhaoxin


### 清除git的全局的用户名和邮箱
> git config --global --unset user.name

> git config --global --unset user.email

### 重新设置每个项目的非全局的用户名和邮箱
>git config user.name "your_name"  
git config user.email "your_email"

### 例：从第2个远端仓库clone代码用别名代替域名
> git clone git@github_zhaoxin:choukin/choukin.github.io.git




## 参考资料
<a href="http://blog.csdn.net/guang09080908/article/details/46545335" class="btn btn-success">参考文章！</a>