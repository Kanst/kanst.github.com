---
layout: page
title: Последние статьи
tagline: 
---
{% include JB/setup %}

<div class="row">
  <div class="span9">
    {% for post in site.posts limit:10%}
      <div class="hero-unit">
        <p><h2><a href="{{ post.url }}">{{ post.title }}</a></h2></p>
        <p>{{ post.content | strip_html | truncatewords: 55 }}</p> 
    <p><span>{{ post.date | date_to_string }}, {{site.author.name}} |</span>
    <a class="news-read-more " href="{{ post.url }}">Читать дальше &rarr;</a></p>
      </div>
    {% endfor %}
  </div>
</div>
