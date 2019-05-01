---
layout: default
title: 全てのポストリスト
permalink: /post
---
<a href="/posts/news">お知らせリスト</a> 


<a href="/posts/blogs">ポストリスト</a> 

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%F" }}
    </li>
  {% endfor %}
</ul>
