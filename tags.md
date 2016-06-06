---
layout: page
title: Tags List
permalink: /tags/
banner_image: sample-banner-image-2.jpg
banner_image_alt: Tag List
---
Tag List:

{% for tag in site.tags %}
  {% assign t = tag | first %}
  {% assign posts = tag | last %}

{{ t }} has {{ posts | size }} posts
<ul>
{% for post in posts %}
  {% if post.tags contains t %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span class="date">{{ post.date | date: "%B %-d, %Y"  }}</span>
  </li>
  {% endif %}
{% endfor %}
</ul>
{% endfor %}
