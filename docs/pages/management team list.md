準備中
{% for item in site.data.member.management %}
    <h3>{{ item.title }}</h3>
| Discordユーザー          | discordid             | twitter |説明         |
|:------------------------|:----------------------|:--------|:------------|
        {% for entry in item.items %}
| {{ entry.discordname }} | {{ entry.discordid }} | {% if entry.discordid %}![{{ entry.twitterid }}](https://twitter.com/{{ entry.twitterid }}){% endif %} | {{ entry.description }} |
        {% endfor %}
  {% endfor %}
