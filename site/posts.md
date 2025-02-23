---
layout: post-list

slug: posts
description: >
    Caricatures are where I find my peace. See my latest work below.
---

<div class="post-previews">
  {% for post in collections.posts %}
  <div class="post-preview" style="--bg-image: url({{post.data.seo_title | seoImage}})">
    <img src="{{post.data.thumb}}" alt='' class='post-preview' loading='lazy' width=120 height=250/>
    {% if post.data.url%}
    <h2><a href="{{post.data.url}}">{{ post.data.title }}</a></h2>
    {% else %}
    <h2><a href="/{{post.data.slug}}/">{{ post.data.title }}</a></h2>
     {% endif %}
    <p class="description">{{ post.data.description }}</p>
    <span aria-hidden="true">expand &rarr;</span>
  </div>
  {% endfor %}
</div>
