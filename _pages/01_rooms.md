---
layout: page
title: Rooms
permalink: /rooms/
categories: [main]
---

Laboratory spaces we are responsible for:
<ul>
{% capture pages %}
  {% for page in site.pages %}
	{% if page.categories contains 'room' %}
		|{{ page.title }}#{{ page.url }}
	{% endif %}
  {% endfor %}
{% endcapture %}

{% assign sortedpages = pages | split: '|' | sort %}

{% for page in sortedpages offset:1 %}
    {% assign pageitems = page | split: '#' %}
		<li>
			<a href="{{ site.baseurl }}{{ pageitems[1] }}">{{ pageitems[0] }}</a>
		</li>
{% endfor %}
</ul>

Maps of Phillips Hall are here:
<ul>
	<li><a href="{{site.baseurl}}/files/039-phillips_hall-gr.pdf">Ground Floor</a></li>
	<li><a href="{{site.baseurl}}/files/039-phillips_hall-01.pdf">First Floor</a></li>
	<li><a href="{{site.baseurl}}/files/039-phillips_hall-02.pdf">Second Floor</a></li>
	<li><a href="{{site.baseurl}}/files/039-phillips_hall-03.pdf">Third Floor</a></li>

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
