---
layout: default
title: Blog
permalink: /blog/
---

<div class="home">

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <h2><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h2>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        <p>
          {{ post.excerpt | remove: '<p>' | remove: '</p>' | truncatewords: 53 }} <span id="read-more"><a href="{{ post.url }}">Read more</a></span>
        </p>
      </li>
    {% endfor %}
  </ul>

</div>
