---
layout: post
title: "Octopress_github_pages"
date: 2014-06-12 14:29:32 +0800
comments: true
categories: 
---
<div>
use Octopress for github, all refer from http://beyondvincent.com/blog/2013/08/03/108-creating-a-github-blog-using-octopress/
</div>
<div>
<h1>meet a error when rake deploy:</h1>
<strong>error: failed to push some refs to</strong> 
<hr/>
<h1>how to resolve:</h1>
<strong>cd _deploy</strong><br/> 
<strong>git push -f</strong> # 强推送过去
<div>
<h1>创建并部署博文的一个完整过程：</h1>
<ol>
<li>$ rake new_post["New Post"]</li>
<li>$ rake generate</li>
<li>$ git add .</li>
<li>$ git commit -am "Some comment here."</li> 
<li>$ git push origin source</li>
<li>$ rake deploy</li>
</ol>
</div>
