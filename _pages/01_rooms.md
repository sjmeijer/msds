---
layout: page
title: Rooms
permalink: /rooms/
categories: [main]
---

<ul>
{% capture pages %}
  {% for page in site.pages %}
	{% if page.categories contains 'room' %}
		|{{ page.title }}#{{ page.url }}
	{% endif %}
  {% endfor %}
{% endcapture %}

{% assign sortedpages = pages | split: '|' | sort %}

{% for page in sortedpages %}
    {% assign pageitems = page | split: '#' %}
		<li>
			<a href="{{ pageitems[1] }}">{{ pageitems[0] }}</a>
		</li>
{% endfor %}
</ul>



<!--
	{% for page in site.pages %}
		{% if page.title %}
			{% if page.categories contains 'material' %}
				<li>
					<a href="{{ page.url }}">{{ page.title }}</a>
				</li>
			{% endif %}
		{% endif %}
	{% endfor %}
-->