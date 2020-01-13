---
title: myfirstpost
date: 2020-01-12 23:01:54
tags:
---
简单搭建方法记录

## 首先,安装必要的软件
```
-包括
$git  从官网上可以下载,网上安装教程也比较详细.
$node.js  里面的npm工具确实挺好用的.
然后在一个自己选定的位置创建一个空文件夹,然后打开文件夹,在空白处右键打开 git bash
$hexo 通过npm安装 :npm install -g hexo-cli
安装完成后可以通过命令查看是否安装成功.
	查看git版本:git --version
	查看node版本:node -v
	以及hexo: hexo -v
```
more in:[more](https://hexo.io/docs/writing.html)

## 然后,获取模板到本地

```
-步骤
接着,在git bash中输入
$ hexo init
$ npm install
这样文件夹中就会有hexo的各种文件以及文件夹
```

## 连接github

首先,你需要一个github账号(注册一个账号)(提醒一下,最好使用Chrome或火狐浏览器)
创建一个新的仓库(在这里需要创建一个以你的账号名开头的仓库:yourname.github.io)<同时,这也是访问的地址>

## 接着,在配置文件中配置相关内容

title:标题
description:说明
keyword:关键字
author:你的名字
url:网站地址...
配置你的标题,说明,名字等,
然后直接拉到最后修改地址,
修改为:
```
deploy:
	type:git
	repo:https://github.com/yourname/yourname.github.io.git
	branch:master
```
其实主要修改你的地址和选择主题
详细:[site](https://hexo.io/docs/configuration#Site)

## 然后,测试一下效果
```
-在git bash 输入
hexo clean 清理原来的public文件
hexo generate 生成public文件
hexo server 启动本地服务器(稍等片刻,你可以看到:INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.)
然后你可以通过打开http://localhost:4000页面看到基础效果.
```

## 上传至github

```
-为了更好部署,可以安装一下:npm install hexo-deployer-git --save
然后执行:
hexo clean
hexo generate (可以简写为:hexo g)
hexo deploy   (可以简写为:hexo d) 部署
然后可能会需要输入账号和密码.
然后就可以看到自己的个人博客啦~
```

## 选择自己想要的主题-(听说Next-T很受欢迎)

```
-当然需要一款个性的主题啦
hexo主题连接:[themes](https://hexo.io/themes/)
选择主题可能需要按照相对应的方法添加或安装一些组件
主要就是改改改.
按照主题安装文档操作就行.
主题配置需要进入到 theme/主题名/_config.yml中修改
```

## 创建新文章 

```
-利用git bash
$ hexo new post <title>
(post指的是创建的模板,比如文章就为post(也可以修改),<title>表示你文章的标题)
利用md写法书写,其实和html差不多,理解起来也差不多.
写完后记得也要重新部署一下:
hexo clean
hexo generate (可以简写为:hexo g)
hexo deploy   (可以简写为:hexo d)
```

## 如果有需要换地方写博客的需要

建议可以在创建一个仓库或分支保存你的当前所有文件
方便在其他地方clone然后继续完成文章.


## 最后

若文中有错误,望指出~

