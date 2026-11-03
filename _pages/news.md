---
permalink: /news/
title: "News"
layout: single
author_profile: false
---

Hier finden Sie Neuigkeiten und Beiträge des Ohrdrufer Leichtathletik Vereins.

{% assign news_posts = site.posts | where_exp: "post", "post.categories contains 'news'" %}
{% if news_posts.size > 0 %}
{% for post in news_posts %}
### [{{ post.title }}]({{ post.url | relative_url }})

<small>{{ post.date | date: "%d.%m.%Y" }}</small>

{{ post.excerpt }}

[Weiterlesen]({{ post.url | relative_url }})

{% endfor %}
{% else %}
Weitere Neuigkeiten folgen in Kürze.
{% endif %}
