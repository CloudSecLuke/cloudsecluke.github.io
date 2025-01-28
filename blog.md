---
layout: default
title: "Blog"
permalink: /blog/
---

<div class="blog-header">
    <p>Weekly blog articles covering cybersecurity topics, projects, and tutorials.</p>
</div>

<div class="blog-index">
  <h1>Latest Blog Posts</h1>
  <ul>
    {% for post in site.posts %}
      <li>
        <a href="{{ post.url | relative_url }}">
          <img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}">
          <h2>{{ post.title }}</h2>
          <p>{{ post.excerpt }}</p>
        </a>
      </li>
    {% endfor %}
  </ul>
</div>

<div class="blog-content">
    <div class="blog-posts">
        {% for post in site.posts %}
        <div class="blog-post">
            <div class="blog-post-image">
                <img src="{{ post.header.image }}" alt="{{ post.title }}">
            </div>
            <div class="blog-post-details">
                <p class="blog-post-category">{{ post.categories | join: " / " }}</p>
                <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
                <p class="blog-post-summary">{{ post.excerpt }}</p>
            </div>
        </div>
        {% endfor %}
    </div>

<div class="pagination">
  {% for post in paginator.posts %}
    <div class="post-preview">
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p>{{ post.excerpt }}</p>
    </div>
  {% endfor %}

  <div class="pagination-nav">
    {% if paginator.previous_page %}
      <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; Previous</a>
    {% endif %}
    {% if paginator.next_page %}
      <a href="{{ paginator.next_page_path | relative_url }}">Next &raquo;</a>
    {% endif %}
  </div>
</div>


<aside class="blog-sidebar">
        <div class="search-widget">
            <h3>Search</h3>
            <form action="/search" method="get">
                <input type="text" name="q" placeholder="Search ..." class="search-input">
                <button type="submit" class="search-button">Search</button>
            </form>
        </div>
        
<div class="newsletter-widget">
            <h3>Newsletter</h3>
            <form action="https://formspree.io/f/your-form-id" method="POST">
                <input type="email" name="_replyto" placeholder="Email Address" required class="newsletter-input">
                <button type="submit" class="newsletter-button">Send Me Newsletters</button>
            </form>
        </div>
    </aside>
</div>
