---
layout: page
title: "Older stuff I wrote"
permalink: /en/older-stuff/
comments: false
share: false
image:
  feature: abstract-1-3
---

This is a list of older blog posts (written when I was younger than 21) that I have published on my own blog. These blog posts are from a time when my knowledge and writing skills were pretty uninteresting to read. If you want to stick around and read them anyway, knock yourself out, but if you're looking for some more high-quality content, [I highly suggest checking out the list of posts I wrote after I turned 21]({{ site.baseurl }}/en/).

<ul>
    {% for post in site.categories.en %}
      {% assign year = post.date | date: "%Y" | times:1 %}
      {% assign month = post.date | date: "%m" | times:1 %}
      {% assign day = post.date | date: "%d" | times:1 %}
      {% if year < 2015 %}
        <li><a href="{{ site.url }}{{post.url }}">{{ post.title }}</a> ({{ post.date | date: "%B %d, %Y" }})</li>
      {% endif %}
      {% if year == 2015 and month < 8 %}
        <li><a href="{{ site.url }}{{post.url }}">{{ post.title }}</a> ({{ post.date | date: "%B %d, %Y" }})</li>
      {% endif %}
      {% if year == 2015 and month == 8 %}
        {% if day < 10 %}
          <li><a href="{{ site.url }}{{post.url }}">{{ post.title }}</a> ({{ post.date | date: "%B %d, %Y" }})</li>
        {% endif %}
      {% endif %}
    {% endfor %}
</ul>
