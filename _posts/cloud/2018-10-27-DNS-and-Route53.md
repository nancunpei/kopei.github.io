---
layout: post
title: DNS和Route53简介
categories: [cloud]
description: DNS的概念和Route53
keywords: DNS, route53
catalog: true
multilingual: false
tags: cloud
---

## DNS基本概念
`Top Level Domain`(TLD)顶级域名是域名中的最后一个部分， 比如`.com`. `Internet Corporation for Assigned Names and Numbers`(ICANN)
负责管理和分配域名， 这些域名会在`Network Information Center`(InterNIC)注册， 每个域名会在一个叫`Whois`的数据库注册， 以维护域名的唯一性。
这里有一个误区，域名如`example.com`, 一般所说的二级域名是应该是`example`(而国内的运营商叫做一级域名)， 其他的一次往后推.

### host和Subdomain
有了域名， 域名拥有者可以把自己的服务或主机定义成`host`, 比如大部分的web服务都可以通过`www`这个`host`访问。
`TLD`是可以被按层级扩展成多个子域名的。如`example.com`中`example`就是`SLD`, 又如`baidu.com.cn`中`.com`是`SLD`. `SLD`和`host`主要的区别在于host定义的是一个资源，
而`SLD`是一个域名的扩展。不管是`SLD`还是`host`, 我们都从域名的左边读起， 可以看到越左边的部分意义越具体。

### Fully Qualified Domain Name(FQDN)
按ICANN的标准FQDN是需要按`.`结尾的，虽然通常我们并没有这么做. 具体语法如下图所示
![http://p0iombi30.bkt.clouddn.com/fqdn-explained.jpg](http://p0iombi30.bkt.clouddn.com/fqdn-explained.jpg)

### 浏览器解析DNS步骤
浏览器输入域名后， 计算机先检查本地hosts文件是否存在对应ip











