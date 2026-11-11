---
layout: default
title: Projects
permalink: /projects/
---

{% include back.html %}

<h2>baby pet projects</h2>

<section class="row" id="portifolio">
{% assign projects = site.projects | sort: "date" | reverse %}
{% for project in projects %}
{{ project.content }}
{% endfor %}
</section>
