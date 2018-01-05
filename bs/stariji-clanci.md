---
layout: page
title: "Older stuff I wrote"
permalink: /bs/stariji-clanci/
comments: false
share: false
image:
  feature: abstract-1-3
---

Ovo je lista članaka koje sam objavio prije početka 2016. Kao takvi, dolaze iz vremena kada su moje vještine u pisanju bloga bile jako ograničene. Ukoliko želite da pročitate još sadržaja, preporučujem listu članaka objavljenih od početka 2016. godine [na bosanskom]({{ site.baseurl}}/bs/) ili [engleskom]({{ site.baseurl }}/en/) jeziku.

<ul>
    {% for post in site.categories.bs %}
      {% assign year = post.date | date: "%Y" | times:1 %}
      {% assign month = post.date | date: "%m" | times:1 %}
      {% assign day = post.date | date: "%d" | times:1 %}
      {% if year < 2015 %}
        <li><a href="{{ site.url }}{{post.url }}">{{ post.title }}</a> ({{ post.date | date: "%d.%m.%Y."  }})</li>
      {% endif %}
      {% if year == 2015 and month < 8 %}
        <li><a href="{{ site.url }}{{post.url }}">{{ post.title }}</a> ({{ post.date | date: "%d.%m.%Y."  }})</li>
      {% endif %}
      {% if year == 2015 and month == 8 %}
        {% if day < 10 %}
          <li><a href="{{ site.url }}{{post.url }}">{{ post.title }}</a> ({{ post.date | date: "%d.%m.%Y."  }})</li>
        {% endif %}
      {% endif %}
    {% endfor %}
</ul>
