---
layout: default
title: ポストリスト
permalink: /post
---
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> - {{ post.date | date: "%F" }}
    </li>
  {% endfor %}
</ul>
