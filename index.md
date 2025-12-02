---
layout: home
title: Welcome
---

<style>
/* Index Page Custom Styles */
.whale-header {
    text-align: center;
    margin-bottom: 3rem;
    font-size: 2.5rem;
    font-weight: 700;
    color: #0a2e36;
}

.about-section {
    background: #0a2e36;
    color: #e8f6f9;
    padding: 2rem;
    border-radius: 8px;
    margin-bottom: 3rem;
    display: flex;
    gap: 2rem;
    align-items: flex-start;
}

.about-text h2 {
    color: #00ffcc;
    margin-top: 0;
}

.about-avatar {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    object-fit: cover;
    border: 3px solid #00ffcc;
    flex-shrink: 0;
}

.posts-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
}

.post-card {
    background: #ffffff;
    border: 1px solid #e1e4e8;
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    display: flex;
    flex-direction: column;
}

.post-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
}

.post-card-image {
    height: 200px;
    background-size: cover;
    background-position: center;
    border-bottom: 1px solid #eee;
}

.post-card-content {
    padding: 1.5rem;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
}

.post-card-title {
    margin: 0 0 0.5rem 0;
    font-size: 1.25rem;
}

.post-card-title a {
    color: #0a2e36;
    text-decoration: none;
}

.post-card-excerpt {
    font-size: 0.9rem;
    color: #555;
    flex-grow: 1;
}

.post-card-meta {
    margin-top: 1rem;
    font-size: 0.8rem;
    color: #888;
    border-top: 1px solid #eee;
    padding-top: 0.5rem;
}

@media (max-width: 768px) {
    .about-section {
        flex-direction: column;
        align-items: center;
        text-align: center;
    }
    .whale-header {
        font-size: 2rem;
    }
}
</style>

<h1 class="whale-header">🐋 Hitchhiker's Guide to Cetaceans</h1>

<div class="about-section">
    <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?w=300&q=80" alt="Researcher Profile" class="about-avatar">
    <div class="about-text">
        <h2>About Me</h2>
        <p><strong>AI engineer/researcher diving deep into cetacean communication and bioacoustics.</strong></p>
        <p>By day, I build neural networks. By night, I study the ones inside whale brains. My focus is on cetacean communication systems—how whales and dolphins encode information, transmit culture, and navigate their acoustic worlds.</p>
        <p>This blog is where machine learning meets marine biology. I break down the latest research in bioacoustics, analyze communication patterns with a signal processing lens, and explore what artificial intelligence can teach us about natural intelligence (and vice versa). Think of it as marine mammal science written by someone who spends too much time thinking about spectrograms, convolutional networks, and whether GPT-4 could ever understand a sperm whale coda.</p>
    </div>
</div>

<h2>Latest Transmissions</h2>

<div class="posts-grid">
  {% for post in site.posts %}
    <article class="post-card">
      {% if post.image %}
      <div class="post-card-image" style="background-image: url('{{ post.image }}');"></div>
      {% else %}
      <div class="post-card-image" style="background-color: #0a2e36;"></div>
      {% endif %}
      
      <div class="post-card-content">
        <h3 class="post-card-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </h3>
        <p class="post-card-excerpt">
          {{ post.excerpt | strip_html | truncatewords: 25 }}
        </p>
        <div class="post-card-meta">
          {{ post.date | date: "%B %d, %Y" }}
        </div>
      </div>
    </article>
  {% endfor %}
</div>
