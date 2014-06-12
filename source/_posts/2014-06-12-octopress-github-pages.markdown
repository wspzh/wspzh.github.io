---
layout: post
title: "Octopress_github_pages"
date: 2014-06-12 14:29:32 +0800
comments: true
categories: 
---
use Octopress for github, all refer from http://beyondvincent.com/blog/2013/08/03/108-creating-a-github-blog-using-octopress/
meet a error when rake deploy:
<strong>error: failed to push some refs to</strong> 

how to resolve:
<strong>cd _deploy</strong>
<strong>git push -f</strong> 强推送过去

创建并部署博文的一个完整过程：
$ rake new_post["New Post"]
$ rake generate
$ git add .
$ git commit -am "Some comment here." 
$ git push origin source
$ rake deploy
