---
layout: page
title: "文章列表"
permalink: /articles/
---

### 行业调查报告

{% for post in site.posts %}
{% capture year %}{{ post.date | date: "%Y" }}{% endcapture %}
{% if year == "2026" %}
#### [{{ post.title }}]({{ post.url | relative_url }})
*{{ post.date | date: "%Y-%m-%d" }}* — {{ post.excerpt | strip_html | truncate: 120 }}
{% endif %}
{% endfor %}

---

