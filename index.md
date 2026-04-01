---
layout: home
title: Welcome
---

# Welcome to My Portfolio

Explore my work across different categories or browse the latest updates below.

---

## Quick Navigation

<div class="nav-grid">
  <a href="/about" class="nav-card">
    <h3>About</h3>
    <p>Learn more about me</p>
  </a>
  <a href="/art" class="nav-card">
    <h3>Art Gallery</h3>
    <p>View my artwork & projects</p>
  </a>
  <a href="/news" class="nav-card">
    <h3>News & Articles</h3>
    <p>Latest posts and updates</p>
  </a>
  <a href="/cv" class="nav-card">
    <h3>CV</h3>
    <p>Download my resume</p>
  </a>
</div>

---

## Recent Posts

{% assign all_posts = site.art | concat: site.news | concat: site.projects | sort: "date" | reverse %}

{% for post in all_posts limit: 6 %}
  <div class="post-preview">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%B %d, %Y" }}  {{ post.category }}</p>
    {% if post.excerpt %}
      <p>{{ post.excerpt | truncatewords: 30 }}</p>
    {% endif %}
  </div>
{% endfor %}

---

## Get in Touch

Have a question or want to collaborate? [Contact me](/contact)
