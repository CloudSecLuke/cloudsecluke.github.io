---
layout: default
title: "Blog"
permalink: /blog/
---

<div class="blog-header">
    <p>Weekly blog articles covering cybersecurity topics, projects, and tutorials.</p>
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
