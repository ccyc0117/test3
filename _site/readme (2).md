# if判断
## 单向分支
{% if 5>3 %}
	真区间
{% endif %}

## 双向分支
{% if 5>3 %}
	真区间
{% else %}
	假区间
{% endif %}

## 多向分支
。。。

# 过滤器
- truncate
- strip_html
- default


# for-in 循环
{% for 键 in 对象%}
	循环体
{% endfor %}

```
{% for post in site.posts %}
	循环体
{% endfor %}
```

# 文章的遍历
`site.posts` 会去到网站根目录下的_posts里面找文件
```
<!-- 文章列表开始 -->
{% for post in site.posts %}
<div class="post-preview">
<a href="{{post.url}}">
  <h2 class="post-title">{{post.title}}</h2>
  <h3 class="post-subtitle">{{post.subheading}}</h3>
</a>
<p class="post-meta">Posted by <a href="#">{{post.author}}</a> on {{post.date | date_to_long_string}}</p>
</div>
<hr>
{% endfor %}
<!-- 文章列表结束 -->
```
# 博客文章的命名
> 1. 需要按照`2019-11-21-文件名.html`的规范
> 2. 在博客文章里面需要定义以下内容：
```
---
layout: post
title: 我的第一片文章
subheading: 随便来点副标题随便来点副标题随便来点副标题
pic: home-bg.jpg
author: 木子z
---
```