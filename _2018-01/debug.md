---
index: true
hidden: true
layout: default
title: "Some articles missing? v2"
name: "2018-01"
---
{% assign pages = site.[name] %}
{% for page in pages %}
.
{% unless (page.index or page.category="association" or page.category="vendor" or page.category="library" or page.category="project" or page.category="association") %}
- Kaboom! [{{ page.title }}]({{ page.path }}) {% if page.hidden %} *Hidden* {% endif %}
{% endunless %}
{% endfor %}