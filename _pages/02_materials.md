---
layout: page
title: Materials
permalink: /materials/
categories: [main]
---
A list of all materials (present in any of our labs).

<ul>
{% capture pages %}
  {% for page in site.pages %}
	{% if page.categories contains 'material' %}
		|{{ page.title }}#{{ page.url }}
	{% endif %}
  {% endfor %}
{% endcapture %}

{% assign sortedpages = pages | split: '|' | sort %}

{% for page in sortedpages offset:1 %}
    {% assign pageitems = page | split: '#' %}
		<li>
			<a href="{{ site.baseurl }}{{ pageitems[1] }}">{{string[1]}}{{ pageitems[0] }}</a>
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