---
layout: post
title: "在Windows7上使用Octopress时遇到的编码问题"
date: 2014-07-11 15:49
comments: true
categories: Octopress
---

在windows7上运行rake preview命令时会遇到一个错误，导致首页在浏览器里不能正常显示。
```
Liquid Exception: incompatible character encodings: IBM437 and UTF-8 in post
Liquid Exception: incompatible character encodings: IBM437 and UTF-8 in index.html
```
上网查了下解决办法， 需要把Windows命令行的Code Page设置成UTF-8。也就是需要在运行rake命令前先输入以下命令：
```
chcp 65001
```
这时候再执行rake命令时就一切正常了。

另外一点要注意的是，在Windows7下所有文件要用不带BOM的UTF-8格式保存，要不然一些gem在解析文件上会发生错误。
