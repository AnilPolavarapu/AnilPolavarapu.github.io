---
layout: page
title: Archive
---

{% for post in site.posts %}
	<svg class="icon"><use xlink:href="#icon-price-tag"></use></svg>
  * {{ post.date | date_to_string }} &raquo; [ {{ post.title }} ]({{ post.url }})
{% endfor %}