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

### 分类

- 🏭 [行业调查](/articles/tags/#行业调查)
- 🔧 [选型指南](/articles/tags/#选型指南)
- 📊 [案例复盘](/articles/tags/#案例复盘)
- 💡 [解决方案](/articles/tags/#解决方案)
