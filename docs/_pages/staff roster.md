---
layout: default
title: スタッフチームリスト
permalink: /スタッフチームリスト
redirect_from:
  - /スタッフチーム一覧
  - /運営チームリスト
  - /運営チーム一覧
  - /staff-roster
---

{% if site.data.staff-roster.management[0] %}
  {% for item in site.data.staff-roster.management %}
<h3>{{ item.title }}</h3>
      {% if item.items[0] %}
<table>
  <tbody><tr>
    <th>Discordユーザー</th>
    <th>Discordid</th>
    <th>Twitter</th>
    <th>説明</th>
  </tr>
          {% for entry in item.items %}
  <tr>
    <td>{{ entry.discordname }}</td>
    <td>{{ entry.discordid }}</td>
    <td>{% if entry.twitterid %}<a href="https://twitter.com/{{ entry.twitterid }}" title="{{ entry.twitterid }}">@{{ entry.twitterid }}</a>{% endif %}</td>
    <td>{{ entry.description }}</td>
  </tr>
          {% endfor %}
      {% endif %}
      </tbody></table>
    {% endfor %}
{% endif %}



