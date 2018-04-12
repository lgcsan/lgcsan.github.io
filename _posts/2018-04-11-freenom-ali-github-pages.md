---
layout: post
title:  "Freenom免费域名 + 阿里DNS + github pages"
categories: web
tags:  Freenom 免费域名 阿里 DNS github pages
author: lcsan
---

* content
{:toc}

一直看别人在github pages上搭Blog，我也fork了一个模板过来，然后就有了你当前看到的这个了。

本人比较赖，啥东西都没改就直接用了。然后嫌弃直接用pages的二级域名不好看，就找着Freenom搞了个免费域名挂着，走阿里的免费CDN解析，凑合着用吧。

现在既然搞完了，就顺便记录以下，免得忘记了。



## github pages个人博客

网上一大把，不想自己折腾。直接fork:[https://github.com/lcsan/lcsan.github.io](https://github.com/lcsan/lcsan.github.io)

把根目下的CNAME里面的域名，改成你申请的域名就行了。其他的东西看着改。

还有，我把评论改成gitment插件了。

插件配置：[commons](https://github.com/lcsan/lcsan.github.io/blob/master/_includes/comments.html)
```yaml
# gitment 评论插件,全必填
gitment_title: 评论
gitment_owner: xxx
gitment_repo: xxx.github.io
gitment_client_id: xxx
gitment_client_secret: xxx
```
具体配置参考：
[gitment](https://imsun.net/posts/gitment-introduction/)

## Freenom免费域名注册
网站：[http://www.freenom.com/zh/index.html?lang=zh](http://www.freenom.com/zh/index.html?lang=zh)

步骤参考这个来，很清晰的描述：
[https://jingyan.baidu.com/article/0eb457e52987b203f0a90541.html](https://jingyan.baidu.com/article/0eb457e52987b203f0a90541.html)

## 阿里云设置
这里关键有一点，Freenom的Nameservers要设置成阿里的DNS
![](http://c.hiphotos.baidu.com/image/%70%69%63/item/72f082025aafa40fb93708bba764034f79f019e7.jpg)
这里DNS改成:ns1.alidns.com 和 ns2.alidns.com

然后去阿里云，管理台配置DNS解析。注意是cname，因为github pages用的是域名，所以直接用cname就行了。找网上有些用a记录，然后ping XXX.github.io得到ip再配置也是可以的。不过github pages会告警，没有配置域名。

1.新配置申请到的Freenom域名
![](http://f.hiphotos.baidu.com/image/%70%69%63/item/d4628535e5dde7111d268690abefce1b9c1661e4.jpg)

![](http://b.hiphotos.baidu.com/image/%70%69%63/item/bd315c6034a85edf2c6d3b4545540923dc5475f7.jpg)

2.配置域名解析
![](http://c.hiphotos.baidu.com/image/%70%69%63/item/3801213fb80e7becd6dcc787232eb9389b506b56.jpg)

3.配置github pages解析
![](http://a.hiphotos.baidu.com/image/%70%69%63/item/03087bf40ad162d9da6fa67a1ddfa9ec8b13cdd7.jpg)

![](http://f.hiphotos.baidu.com/image/%70%69%63/item/aa18972bd40735fa03658adf92510fb30f24083b.jpg)

ok，完美！

## 补充

本来有微博图床的，家里没装插件。临时用百度识图充充图床

**百度识图是个好东西**,你看我图片都是直链百度的图片。
