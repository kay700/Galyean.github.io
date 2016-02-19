---
layout: post
title:  "在Digitalocean上搭建代理服务"
date:   2016-02-19 17:56:23
categories: jekyll update
tags: [瞎折腾的] 
---

&emsp;&emsp; *这是尝试用markdown写的第一篇文章，暂时没有想到写些什么，所以就把以前的文章先搬一篇过来凑个数，新手入门，排版很丑。*

&emsp;&emsp;因为平时 coding 以及科研需要用到 google，而之前常用的几个 vpn 服务提供商如 J-Proxy 等也因为管制的越来越严停止提供服务，所以索性自己买了个 VPS 自己搭建代理。

&emsp;&emsp;现在广泛使用的代理方式是 socks 代理，shadowsocks 就是一种很方便使用的 socks 代理，速度快，安装配置过程极其简单，而且不容易被干扰。shadowsocks 对应各平台的 gui client 在 github 上有人维护（刚去看了下，好像作者被请去喝茶所以停止更新了），[window-s][1]、mac、iOS和[android][2]平台上都有相应客户端。 **PS:**  ios平台上只有越狱的设备才能正常使用shadowsocks，后来为了解决这个问题，我又搭建了 OpenConnect ser-ver 供 ios 设备使用，详情参考[这篇博客][3]。

&emsp;&emsp;之所以选择Digitalocean的主机，是因为GitHub的Student Developer Pack提供100刀的优惠券（当然这个要自己去[GitHub][4]申请才行）。下面就写一下VPS的配置和Shadowsoc-ks服务的搭建。


  [1]: https://github.com/shadowsocks/shadowsocks-windows/releases
  [2]: https://play.google.com/store/apps/details?id=com.github.shadowsocks&hl=zh_CN
  [3]: http://www.fanyueciyuan.info/fq/ocserv-debian.html/comment-page-1#comments
  [4]: https://education.github.com/pack?utm_source=tuicool
