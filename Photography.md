---
title: Photography
layout: rest
description: some photos contain emotions and thoughts of those captured. some photos reflect those of the photographer. NEWLINE rare ones do both. NEWLINE all photos are portals to me - in different time, place, or state of mind
type: parent
order: 3
---

<div class="section main">
	<div class="container">
		{% assign mypages = site.pages | where: "type", "Photography" %}
		{% for page in mypages %}
		<a class="button" href="{{ page.url | relative_url }}">{{ page.title }}</a>
		{% endfor %}
	</div>
</div>