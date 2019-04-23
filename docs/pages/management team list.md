---
layout: default
title: 運営チーム
permalink: /運営チーム

---

準備中

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
    <td>{% if entry.discordid %}<a href="https://twitter.com/{{ entry.twitterid }}" title="{{ entry.twitterid }}">{{ entry.twitterid }}</a>{% endif %}</td>
    <td>{{ entry.description }}</td>
  </tr>
          {% endfor %}
      {% endif %}
      </tbody></table>
    {% endfor %}
{% endif %}



