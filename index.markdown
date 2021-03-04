---
layout: default
image: BS-thumbnail.png
---

<div>
   <h1>Visual experiments in journalism and fiction.</h1>
   {% for post in site.posts %}
      <a href="{{ post.url }}" class="article">
         <img src="{{ post.img }}" alt="" />
         <div class="article-details">
            <div class="article-labels">
               {% if post.interactive %}
                  <div class="article-tag">
                     <span>interactive</span>
                  </div>
               {% endif %}
                  <div class="article-tag">
                     <span>{{ post.category }}</span>
                  </div>
            </div>
               <h2>{{ post.title }}</h2>
            {% if post.contributor %}
            <div class="article-contributors"> {{ post.contributor }} </div>
            {% endif %}
            <div class="article-description"> {{ post.description }}</div>
         </div>
      </a>
   {% endfor %}
</div>



