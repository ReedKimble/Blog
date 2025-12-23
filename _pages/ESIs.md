---
title: "ESIs"
permalink: /ESIs/
layout: single
author_profile: true
sidebar:
  nav: "docs"
---

Emergent Structural Invariants (ESIs) are properties observed to arise repeatedly in systems that maintain coherence, closure, and correctly applied constraint. They are presented without ordering, hierarchy, or claim of completeness.

{% for post in site.categories.ESIs %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}
