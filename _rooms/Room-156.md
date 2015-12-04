---
layout: room
title: Room 156
date:   2015-12-04 11:33:27
categories: [room]
permalink: /156/
roomnumber: 156
---

This room is the electronics lab near Mark's office.

<!--
Room 156 contains the following chemicals:


{% capture pages %}
  {% for page in site.pages %}
	{% if page.rooms contains 156 %}
		|{{ page.title }}#{{ page.url }}
	{% endif %}
  {% endfor %}
{% endcapture %}

{% assign sortedpages = pages | split: '|' | sort %}

<ul>
{% for page in sortedpages %}
    {% assign pageitems = page | split: '#' %}
		<li>			
			<a href="{{ pageitems[1] }}">{{ pageitems[0] }}</a>
		</li>
{% endfor %}
</ul>
-->