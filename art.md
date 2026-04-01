---
layout: page
title: Art Gallery
permalink: /art/
---

# Art Gallery

Browse my artwork and creative projects.

<div class="filter-buttons">
  <button class="filter-btn active" data-filter="all">All</button>
  <button class="filter-btn" data-filter="painting">Paintings</button>
  <button class="filter-btn" data-filter="digital">Digital Art</button>
  <button class="filter-btn" data-filter="photography">Photography</button>
  <button class="filter-btn" data-filter="design">Design</button>
</div>

<div class="gallery-grid">
  {% for item in site.art | sort: "date" | reverse %}
    <div class="gallery-item" data-category="{{ item.category }}">
      <a href="{{ item.url }}">
        <div class="item-content">
          <h4>{{ item.title }}</h4>
          <p class="date">{{ item.date | date: "%Y" }}</p>
          <p class="tags">{{ item.tags | join: ", " }}</p>
        </div>
      </a>
    </div>
  {% endfor %}
</div>

<p class="empty-state" id="empty-state" style="display: none;">
  No works found in this category.
</p>

<script>
document.querySelectorAll('.filter-btn').forEach(btn => {
  btn.addEventListener('click', function() {
    const filter = this.dataset.filter;
    const items = document.querySelectorAll('.gallery-item');
    let visibleCount = 0;
    
    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
    this.classList.add('active');
    
    items.forEach(item => {
      if (filter === 'all' || item.dataset.category === filter) {
        item.style.display = 'block';
        visibleCount++;
      } else {
        item.style.display = 'none';
      }
    });
    
    document.getElementById('empty-state').style.display = visibleCount === 0 ? 'block' : 'none';
  });
});
</script>
