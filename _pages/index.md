---
title: "Home"
permalink: /
layout: single
author_profile: true
sidebar:
  nav: "docs"
---

Posts in Categories

{% for cat in site.categories %}
- {{ cat.name }}
{% for post in cat %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}
{% endfor %}
