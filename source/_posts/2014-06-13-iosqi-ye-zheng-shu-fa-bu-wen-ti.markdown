---
layout: post
title: "ios企业证书发布问题"
date: 2014-06-13 17:17:02 +0800
comments: true
categories: 
---
<h1>IOS 企业版证书发布应用时遇到的小问题</h1>
<div>
<h2>问题描述</h2>
<div>利用企业版证书发布应用后使用手机安装测试时发现，应用可以安装成功，但是会留下一个正在安装的小图标</div>
<h2>问题分析</h2>
<div>应用的bundle id 与 plist文件中的bundle id 不一致导致</div>
<h2>解决方法</h2>
<div>检查两者是否一致，同时确认证书是否设置正确</div>
</div>
