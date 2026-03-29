---
layout: default
title: Hitchhiker's Guide to Cetaceans
description: "A blog about cetacean communication, bioacoustics, and marine intelligence by Mudit Sinha"
---

<div class="home-header">
  <div class="home-header-inner">
    <img src="https://avatars.githubusercontent.com/u/55638747?v=4" alt="Mudit Sinha" class="home-avatar">
    <div class="home-header-text">
      <h1 class="home-title">Hitchhiker's Guide to Cetaceans</h1>
      <p class="home-byline">By <strong>Mudit Sinha</strong></p>
    </div>
  </div>
  <p class="home-bio">Aspiring marine ecologist currently working in AI. I love whales and can't stop wondering just how smart they really are. This blog is where I nerd out about cetacean communication, bioacoustics, and everything in between.</p>
</div>

<div class="home-posts">
  {% for post in site.posts %}
  <a href="{{ post.url | relative_url }}" class="post-row">
    <div class="post-row-text">
      <span class="post-row-date">{{ post.date | date: "%d %b %Y" | upcase }}</span>
      <h2 class="post-row-title">{{ post.title }}</h2>
      <p class="post-row-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      {% if post.author %}<span class="post-row-author">By {{ post.author }}</span>{% endif %}
    </div>
    {% if post.image %}
    <div class="post-row-thumb" style="background-image: url('{{ post.image }}');"></div>
    {% endif %}
  </a>
  {% endfor %}
</div>
