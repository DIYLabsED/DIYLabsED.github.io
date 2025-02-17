---
layout: bare-minimum
title: "All Blog Posts"
permalink: /blogs/
---

<h1 class="centered-text">All my blogs:</h1>

<div class="highlighted-posts">
    {% for post in site.posts %}
    <article class="highlighted-post">
        <a href="{{ site.baseurl }}{{ post.url }}">
            <img src="{{ post.cover_image | default: '/post-covers/default.png' }}" alt="Cover Image">
        </a>
        <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
        <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
    </article>
    {% endfor %}
</div>
