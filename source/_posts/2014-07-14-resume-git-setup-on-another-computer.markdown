---
layout: post
title: "如何在另一台电脑上继续更新Octopress"
date: 2014-07-14 11:52
comments: true
categories: Octopress
---

准备工作:
先Clone一份代码，比如克隆我的Blog的命令是
```
git clone git@github.com:magicwind/magicwind.github.com.git
```

然后CD到本地Git目录，切换到source分支
```
cd magicwind.github.com
git checkout source
```
运行rake generate生成public目录

接下来可以手动创建_deploy目录，在该目录下运行以下git命令
```
git init
git remote add origin git@github.com:magicwind/magicwind.github.com.git
git fetch
git checkout master
```
保证_deploy目录下的git有push权限（检查下SSH证书的配置）。

回到上级magicwind.github.com目录就可以使用rake deploy命令同步_deploy目录下的所有文件到远程master分支了。

最后别忘记commit和push根目录的改动到远程source分支。
