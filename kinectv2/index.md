---
layout: default
title: Kinect Version 2
permalink: /kinectv2/
---


<div class="posts">
  {% for post in site.tags.kinectv2 %}
    <article class="post">    
      
      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.content | truncatewords:40}}
      </div>
      
      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>
