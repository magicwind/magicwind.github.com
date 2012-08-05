---
layout: post
title: "Say hello to Octopress"
date: 2012-07-21 16:56
comments: true
categories: 
---

First time to touch Octopress.  
Very like this way to write blog.  

为了方便记忆Octopress的各种常用命令，现制作Cheat Sheet如下：  
创建新博客
```
rake new_post["title"]
```

创建新页面
```
rake new_page[super-awesome]
# creates /source/super-awesome/index.markdown
rake new_page[super-awesome/page.html]
# creates /source/super-awesome/page.html
```

生成静态页面
```
rake generate
```

查看修改
```
rake watch
```

预览
```
rake preview
```

部署到远程服务器（之后别忘记用Git提交到github）
```
rake deploy
```
