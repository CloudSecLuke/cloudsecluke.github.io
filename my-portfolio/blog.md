---
layout: default
title: "Blog"
---

<div class="content">
    <p>Welcome to my blog! Here, I share insights, tutorials, and updates about cybersecurity, cloud security, and more.</p>

    <h2>Recent Posts</h2>
    <ul>
        {% for post in site.posts %}
        <li>
            <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            <p>{{ post.excerpt }}</p>
        </li>
        {% endfor %}
    </ul>
</div>
