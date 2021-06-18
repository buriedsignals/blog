---
layout: default
title: Buried Signals
description: Visual experiments in journalism and fiction.
image: /assets/img/og_image.png
---

<div>
   <h1>Visual experiments in journalism and fiction.</h1>
   {% for post in site.posts %}
      <a href="{{ post.url }}" class="article">
         <img src="{{ post.image }}" alt="" />
         <div class="article-details">
               <h2>{{ post.title }}</h2>
            {% if post.contributor %}
            <div class="article-contributors"> {{ post.contributor }} </div>
            {% endif %}
            <div class="article-description"> {{ post.description }}</div>
         </div>
      </a>
   {% endfor %}
</div>



