---
layout: page
title:
tagline:
---
{% include JB/setup %}

### recent 20 notes list

<ul class="index-posts">
  {% for post in site.posts limit:20 %}
    <li><time class="date" datetime="{{ post.date }}">{{ post.date | date: "%m-%d" }}</time> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}" title="{{ post.title }} @ {{ post.date | date: '%Y-%m-%d' }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

### &raquo; [back to github.com/Rplus](https://github.com/Rplus)
