---
title: gitee和github同步更新
mathjax: true
categories: [配置]
tags: [github, gitee]
abbrlink: 2d45259f
date: 2020-12-06 00:44:13
img: https://cdn.jsdelivr.net/gh/Mug-9/imge-stroage@master/cover/wallhaven-y8x6gk.2f9lwlv4eev4.jpg
---

gitee和github同步更新

<!-- less-->

## 码云

由于众所周知的原因，在github上clone很慢，所以采用码云来加速clone

### 1 在码云上导入github项目

![img1](https://wx3.sinaimg.cn/mw690/0083TyOJly1gldgqbjrwgj30bx08xwen.jpg)

### 2 修改`config`

`git clone`到本地，在视图中显示隐藏项目，进入`.git`找到`config`

![img2](https://wx3.sinaimg.cn/mw690/0083TyOJly1gldgqf0oisj307k083weg.jpg)

### 3 加上github的链接

由于是在gitee上clone的项目，所以在config中只有gitee的链接，在github链接下面加上gitee的链接

注意： 一定是github下面加gitee的链接

![img3](https://wx2.sinaimg.cn/mw690/0083TyOJly1gldgqh0or2j30f8010mx1.jpg)

## 成功

这样就可以在`push`的时候同时更新了