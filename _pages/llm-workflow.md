---
title: "LLM Workflow"
permalink: /llm-workflow/
layout: single
author_profile: true
sidebar:
  nav: "docs"
---

Here I document a practical workflow for using large language models to build real software without falling into vibe coding.

This will eventually be a series: from initial idea, to specs, to implementation, with concrete examples and prompts.

{% for post in site.categories.llm-workflow %}
- [{{ post.title }}]({{ post.url }})
{% endfor %}
