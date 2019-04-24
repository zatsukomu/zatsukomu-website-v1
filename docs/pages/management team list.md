---
layout: default
title: 運営チーム一覧
permalink: /運営チーム一覧

---

データの編集の場合は、[ここから](https://github.com/zatsukomu/zatsukomu.tk/blob/master/docs/_data/member.yml)

{% if site.data.member.management[0] %}
  {% for item in site.data.member.management %}
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



