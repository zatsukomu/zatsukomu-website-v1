---
layout: default
title: 運営チーム
permalink: /運営チーム
---
準備中
    <h3>{{ item.title }}</h3>
| Discordユーザー          | discordid             | twitter |説明         |
|:------------------------|:----------------------|:--------|:------------|
{% for item in site.data.member.management %}
        {% for entry in item.items %}
| {{ entry.discordname }} | {{ entry.discordid }} | {% if entry.discordid %}[{{ entry.twitterid }}](https://twitter.com/{{ entry.twitterid }}){% endif %} | {{ entry.description }} |
        {% endfor %}
  {% endfor %}
