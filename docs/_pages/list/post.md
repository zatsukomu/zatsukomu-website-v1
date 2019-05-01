---
layout: default
title: 全てのポストリスト
permalink: /post
---
<a href="/post/news">お知らせリスト</a> 


<a href="/post/blogs">ポストリスト</a> 

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%F" }}
    </li>
  {% endfor %}
</ul>
