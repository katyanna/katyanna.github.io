---
layout: default
title: Projects
permalink: /projects/
---

{% include back.html %}

<h2>baby pet projects</h2>

{% for project in site.projects %}
    {{ project }}
{% endfor %}
