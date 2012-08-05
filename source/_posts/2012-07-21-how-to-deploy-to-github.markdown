---
layout: post
title: "如何在github上部署Octopress个人博客"
date: 2012-07-21 17:37
comments: true
categories: 
---

在接触过Octopress后，最令人兴奋的事情莫过于将自己的博客搭到github上。一方面可以彰显出自己Geeker的身份，另一方面利用完全免费的托管主机，可以100％深度定制网站，这在几年前是不可能有的好事。  
我在仔细阅读了Octopress的官方文档后，并没有十分顺利的一次就成功搭建，而是尝试了两三次。事后想想，其实文档还算蛮清楚的，主要是自己对github的托管方式还没完全理解，也就是github page是如何工作的。
所以在此做一些额外的补充：

1. github page托管网站的方式主要分两种，一种是针对用户或者组织的网站，另一种是针对项目的网站。

    一个用户或者组织只能拥有一个网站，而且网站的域名也是约定好的。比如用户名叫foobar，那么该用户的网站域名就是foobar.github.com，当然之后也可以绑定自己的其他域名。组织和用户的规则一样。

    如果是项目网站，那么网站的域名就是username.github.com/projectname，看上去像是一个用户的子页面。

2. github page不仅默认规定了网站的域名，同时也规定了repo的名字。在github page上新建一个网站，其实就相当于在github上新建一个repo。

	对于用户和组织来说，repo的名字就是username.github.com。没错，repo的名字就是域名，这一点我一开始也有些迷惑，不是很习惯这命名，仔细看了[github page的文档](https://help.github.com/articles/user-organization-and-project-pages "github page的文档")后才发现这样是对的。

3. 了解上面两点后，后面的就不难了。按照[文档](http://octopress.org/docs/deploying/github/ 'Deploying to Github Pages')一步一步做下去就可以了。主要步骤就是新建repo, 然后依次执行如下命令就可以了。

```
rake setup_github_pages
# 需要你输入repo地址等信息
rake generate
rake deploy
```

如果对git的命令不太熟悉的， 可以参考这篇文章：[Octopress: Setting up a Blog and Contributing to an Existing One](http://code.dblock.org/octopress-setting-up-a-blog-and-contributing-to-an-existing-one)。
