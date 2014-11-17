---
layout: archive
title: "Mastering Paper by 53"
excerpt: "Tutorials and techniques to help learn Paper."
modified: 2014-11-12T22:39:54-05:00
image: 
  thumb: paper-53-expanded-guide-thumb.jpg
tags: [Paper by 53, tutorial, drawing, painting, iPad]
---

In the spirit of openness I've decided to compile everything I've learned using [*Paper by FiftyThree*](http://www.fiftythree.com), into a multi-part series I'm dubbing Mastering Paper.
{:.shorten}

<nav class="toc toc-left">
  <ul>
    <li><h6>Getting Started with Paper for iPad</h6></li>
    <li><a href="{{ site.url }}{% post_url /mastering-paper/2013-09-05-drawing-clouds %}">How to Draw Skies and Clouds</a></li>
    <li><a href="{{ site.url }}{% post_url /mastering-paper/2013-09-29-drawing-water %}">How to Draw Water and Waves</a></li>
  </ul>
</nav>

<div class="tiles tiles-right">
{% for post in site.categories.mastering-paper %}
  <article class="tile" itemscope itemtype="http://schema.org/Article">
    <a href="{{ post.url }}" title="{{ post.title }}" class="post-teaser">
      <img src="{{ site.url }}/images/preload-400.png" data-original="/images/{% if post.image.teaser %}{{ post.image.teaser }}{% else %}{{ site.teaser }}{% endif %}" class="load" alt="teaser" itemprop="image">
      <noscript><img src="/images/{% if post.image.teaser %}{{ post.image.teaser }}{% else %}{{ site.teaser }}{% endif %}" alt="teaser" itemprop="image"></noscript>
    </a>
    <h2 class="post-title" itemprop="name"><a href="{{ post.url }}">{{ post.title | remove: 'Mastering Paper by 53: ' | remove: ' with Paper by 53' }}</a></h2>
    {% if post.date %}<p class="entry-date date published"><time datetime="{{ post.date | date: "%Y-%m-%d" }}" itemprop="datePublished">{{ post.date | date: "%B %d, %Y" }}</time></p>{% endif %}
    <p class="post-excerpt" itemprop="description">{{ post.excerpt | strip_html | truncate: 160 }}</p>
    </article><!-- /.tile -->
{% endfor %}