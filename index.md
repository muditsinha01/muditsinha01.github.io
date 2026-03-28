---
layout: home
title: Welcome
---

<div class="hero-section">
  <div class="hero-content">
    <div class="hero-avatar-wrapper">
      <img src="{{ '/assets/images/profile.png' | relative_url }}" alt="Mudit Sinha" class="hero-avatar">
    </div>
    <h1 class="hero-title">Hitchhiker's Guide to Cetaceans</h1>
    <p class="hero-subtitle">AI engineer diving deep into cetacean communication and bioacoustics.<br>Where machine learning meets marine biology.</p>
  </div>
</div>

<section class="posts-section">
  <h2 class="section-heading">Latest Transmissions</h2>
  <div class="posts-grid">
    {% for post in site.posts %}
      <a href="{{ post.url | relative_url }}" class="post-card-link">
        <article class="post-card" style="animation-delay: {{ forloop.index0 | times: 0.15 }}s;">
          {% if post.image %}
          <div class="post-card-image" style="background-image: url('{{ post.image }}');">
            <div class="post-card-overlay"></div>
          </div>
          {% else %}
          <div class="post-card-image post-card-image--default">
            <div class="post-card-overlay"></div>
            <span class="post-card-icon">🐋</span>
          </div>
          {% endif %}
          <div class="post-card-content">
            <div class="post-card-tag">Article</div>
            <h3 class="post-card-title">{{ post.title }}</h3>
            <p class="post-card-excerpt">
              {{ post.excerpt | strip_html | truncatewords: 30 }}
            </p>
            <div class="post-card-meta">
              <time>{{ post.date | date: "%B %d, %Y" }}</time>
              <span class="post-card-arrow">&rarr;</span>
            </div>
          </div>
        </article>
      </a>
    {% endfor %}
  </div>
</section>

<section class="about-section">
  <h2 class="section-heading">About Me</h2>
  <div class="about-card">
    <div class="about-content">
      <p><strong>By day, I build neural networks. By night, I study the ones inside whale brains.</strong></p>
      <p>My focus is on cetacean communication systems — how whales and dolphins encode information, transmit culture, and navigate their acoustic worlds. This blog is where I break down the latest research in bioacoustics, analyze communication patterns with a signal processing lens, and explore what artificial intelligence can teach us about natural intelligence.</p>
    </div>
  </div>
</section>
