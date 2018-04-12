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
![](https://ws1.sinaimg.cn/large/7201d9dcgy1fqa6nvzromj20rn0epdhv.jpg)
这里DNS改成:ns1.alidns.com 和 ns2.alidns.com

然后去阿里云，管理台配置DNS解析。注意是cname，因为github pages用的是域名，所以直接用cname就行了。找网上有些用a记录，然后ping XXX.github.io得到ip再配置也是可以的。不过github pages会告警，没有配置域名。

1.新配置申请到的Freenom域名
![](https://ws1.sinaimg.cn/large/7201d9dcgy1fqa6nvzq58j20wm0f73zg.jpg)

![](https://ws1.sinaimg.cn/large/7201d9dcgy1fqa6nvz0t6j20mf08rt8s.jpg)

2.配置域名解析
![](https://ws1.sinaimg.cn/large/7201d9dcgy1fqa6nvz9gyj20n206rdfv.jpg)

3.配置github pages解析
![](https://ws1.sinaimg.cn/large/7201d9dcgy1fqa6nvz3fuj20l80chmxc.jpg)

![](https://ws1.sinaimg.cn/large/7201d9dcgy1fqa6nvyz3jj20l10cvweo.jpg)

ok，完美！

## 补充

本来有微博图床的，家里没装插件。临时用百度识图充充图床。结果百度识图偶尔也抽风,有时候失效。
