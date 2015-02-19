---
layout: default
title: Blog
permalink: /blog/
---

<div class="home">

  <ul class="post-list">
    {% for post in site.posts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <p>
          {{ post.excerpt | truncatewords: 80 }} <span id="read-more"><a href="{{ post.url }}">Read more</a></span>
        </p>
      </li>
    {% endfor %}
  </ul>

</div>