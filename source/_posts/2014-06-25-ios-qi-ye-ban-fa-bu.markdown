---
layout: post
title: "iOS 企业版APP发布"
date: 2014-06-25 11:01:07 +0800
comments: true
categories: 
---

使用企业版证书签名，并通过ota模式发布应用

使用企业版证书打包应用，很简单，只要证书、签名、boundid 配置正确，直接操作，基本没有问题
采用ota方法发布应用 关键语句如下：
`<a href="itms-services://?action=download-manifest&url=https://dn-xx.qbox.me/xx.plist">点击这里安装.</a>`
其中 

1. https 是为了ios 7.1及以上版本也可以下载安装，地址自己配置，此处采用的是七牛提供的https服务
2. xx.plist，无任何含义，只是你自己要提供的plist文件，具体如何设置，请google 或 baidu

需要注意的一点：**xx.plist中的bundle id 要 和 xx.plist对应的ipa包的bound id 一致**，不然 嘿嘿……
以上是 一般网上都能查到的，但是我使用时出现了一个问题：
	*有时候发布的新版本不生效，下载到的程序不是最新发布的版本*
当然该问题的出现不排除是我自己设置有误而导致的，希望有知道的朋友友情提示一下。
不管哪里有问题，总要先解决
目前我所找到的一个解决方法是 增加一个可变参数，如下所示： 
   `<a href="itms-services://?action=download-manifest&url=https://dn-xx.qbox.me/xx.plist&app=4">点击这里安装.</a>`
    *关键部位： &app=4*
*     参数名	随意设置，此处为app  
*     参数值	随机生成，此处为4
    
附加备忘另外一个问题：
微信带图片分享失败
> 除了检查微信开放平台的提示信息，如title，description，image不能为空等，
> 附加检查一下图片image的大小不超过32k 
> 以及图片image的像素大小，太大好像也不能分享成功，原因未知   
