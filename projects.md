---
layout: default
title: Projects
permalink: /projects/
---
# Projects

{% for project in site.projects %}
## [{{ project.title }}]({{ project.url }})
{{ project.description }}

[View Repo]({{ project.github }}) | [Notebook]({{ project.colab }})

---
{% endfor %}

[← Back to Home](/)
