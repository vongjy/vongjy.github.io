---
layout: default
title: "Blog"
mathjax: true
show_excerpts: true
---

{% if site.show_excerpts %}
  {% include home.html %}
{% else %}
  {% include archive.html title="Posts" %}
{% endif %}
