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
  </tr>
          {% for entry in item.items %}
  <tr>
    <td>{{ entry.discordname }}</td>
    <td>{{ entry.discordid }}</td>
  </tr>
          {% endfor %}
      {% endif %}
      </tbody></table>
    {% endfor %}
{% endif %}



