---
title: "Structure"
permalink: /structure/
layout: single
author_profile: true
sidebar:
  nav: "docs"
---

Posts regarding Structure defined in Protodomain Grammar

{% for post in site.categories.structure %}
- [{{ post.title }}]({{ post.url | prepend: site.baseurl }})
{% endfor %}
