---
layout: default
title: Blog
excerpt: "Blog."
permalink: /blog/
sitemap: true
---
<h1>Latest Posts</h1>

{% assign number_printed = 0 %}
{% for post in site.posts %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <a href="{{ site.baseurl }}{{ post.url }}">
    <pubtit>{{ post.title }}</pubtit>
  </a>
  {% if post.author %} •
  <span itemprop="author" itemscope itemtype="http://schema.org/Person">
    <span itemprop="name"><em>{{ post.author }}</em></span>
  </span>
  {% endif %}
  {{ post.excerpt }}
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
