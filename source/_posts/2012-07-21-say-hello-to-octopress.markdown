---
layout: post
title: "Say hello to Octopress"
date: 2012-07-21 16:56
comments: true
categories: Octopress
---
Updated 2017-11-17: Use ruby 2.4.2 (installed by homebrew) on macOS Sierra.

需要手工安装:
```
gem install jekyll
gem install compass
gem install rack
```
启动命令需要使用bundle exec rake some_action

--------------分界线---------------

First time to touch Octopress.  
Very like this way to write blog.  

为了方便记忆Octopress的各种常用命令，现制作Cheat Sheet如下：  
创建新博客
```
bundle exec rake new_post["title"]
```

创建新页面
```
bundle exec rake new_page[super-awesome]
# creates /source/super-awesome/index.markdown
rbundle exec ake new_page[super-awesome/page.html]
# creates /source/super-awesome/page.html
```

生成静态页面
```
bundle exec rake generate
```

查看修改
```
bundle exec rake watch
```

预览
```
bundle exec rake preview
```

部署到远程服务器（之后别忘记用Git提交到github）
```
bundle exec rake deploy
```
