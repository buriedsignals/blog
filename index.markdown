---
layout: default
---

<div class="articles-wrapper">
   <h4>Visual experiments in journalism and fiction.</h4>
   <hr class="soft-separator">
   {% for post in site.posts %}
      <a href="{{ post.url }}" class="article-list-item">
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
      </a>
   {% endfor %}
</div>



