---
layout: default
title: 運営チーム
permalink: /運営チーム

---

準備中
{% for item in site.data.member.management %}
    <h3>{{ item.title }}</h3>
    
| Discordユーザー          | discordid             | twitter |説明         |
|:------------------------|:----------------------|:--------|:------------|
        {% for entry in item.items %}
| {{ entry.discordname }} | {{ entry.discordid }} | {% if entry.discordid %}[{{ entry.twitterid }}](https://twitter.com/{{ entry.twitterid }}){% endif %} | {{ entry.description }} |
        {% endfor %}
  {% endfor %}
  

{% if site.data.member.management[0] %}
  {% for item in site.data.member.management %}
    <h3>{{ item.title }}</h3>
      {% if item.items[0] %}
| Discordユーザー          | discordid             | twitter |説明         |
|:------------------------|:----------------------|:--------|:------------|
          {% for entry in item.items %}
| {{ entry.discordname }} | {{ entry.discordid }} | {% if entry.discordid %}[{{ entry.twitterid }}](https://twitter.com/{{ entry.twitterid }}){% endif %} | {{ entry.description }} |
          {% endfor %}
      {% endif %}
    {% endfor %}
{% endif %}
