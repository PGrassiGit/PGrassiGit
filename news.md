---
layout: page
title: News & Articles
permalink: /news/
---

# News & Articles

Stay updated with my latest posts and announcements.

<div class="search-box">
  <input type="text" id="search-input" placeholder="Search posts...">
</div>

<div class="posts-list">
  {% assign sorted_posts = site.news | concat: site.projects | sort: "date" | reverse %}
  
  {% for post in sorted_posts %}
    <article class="post-item searchable">
      <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
      <div class="post-meta">
        <span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
        {% if post.tags %}
          <span class="tags">
            {% for tag in post.tags %}
              <span class="tag">{{ tag }}</span>
            {% endfor %}
          </span>
        {% endif %}
      </div>
      {% if post.excerpt %}
        <p class="excerpt">{{ post.excerpt | truncatewords: 50 }}</p>
      {% endif %}
      <a href="{{ post.url }}" class="read-more">Read more →</a>
    </article>
  {% endfor %}
</div>

<script>
document.getElementById('search-input').addEventListener('keyup', function() {
  const searchTerm = this.value.toLowerCase();
  const posts = document.querySelectorAll('.searchable');
  
  posts.forEach(post => {
    const text = post.innerText.toLowerCase();
    post.style.display = text.includes(searchTerm) ? 'block' : 'none';
  });
});
</script>
