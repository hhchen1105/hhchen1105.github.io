---
layout: default
title: Hung's Notes
---

# Hung's Notes

這裡收錄我對資工教育、AI、科技、研究文化與時事的一些札記。

## Recent Posts

{% for post in site.posts limit:10 %}
- [{{ post.title }}]({{ post.url | relative_url }})，{{ post.date | date: "%Y-%m-%d" }}
{% endfor %}
