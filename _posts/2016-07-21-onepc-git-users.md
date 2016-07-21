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

### 清除git的全局的用户名和邮箱
> git config --global --unset user.name
> git config --global --unset user.email

### 重新设置每个项目的非全局的用户名和邮箱
>git config user.name "your_name"  
git config user.email "your_email"


## 参考资料
<a href="http://blog.csdn.net/guang09080908/article/details/46545335" class="btn btn-success">参考文章！</a>