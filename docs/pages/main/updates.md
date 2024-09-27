---
layout: main
title: Updates
---

---

{% for page in site.pages %}
{% if page.layout == 'update' %}

## [{{page.date}} - {{page.title}}]({{page.url}})
{{page.content}}

---

{% endif %}
{% endfor %}
