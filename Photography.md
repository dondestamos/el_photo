---
title: Photography
layout: rest
description: some photos contain emotions and thoughts of those captured. some photos reflect those of the photographer. NEWLINE rare ones do both. NEWLINE all photos are portals to me - in different time, place, or state of mind
type: parent
order: 3
---

<div class="section main">
	<div class="container">
		{% assign mypages = site.pages | where: "type", "papapa" %}
		{% for page in mypages %}
		<a class="button" href="{{ page.url | relative_url }}">{{ page.title }}</a>
		{% endfor %}
		
		<p markdown="1" style="text-align: center;">
My photos will be here. I believe everyone has their own journey, and it is worth documenting.  
---  
Why El?  
El is short for Elysian.  
---  

		</p>
	<div class="row" id="gallery">
			{% assign coll = site.collections | where: "label", "home" | first %}
			{% assign list = coll.files | sort: "basename" %}
			<!--{% assign l = coll.files.size | divided_by: 2 | ceil %}-->
			<div class="column">
				{% for image in list limit: 1 %}
				<article class="thumb">
					<img class="lozad u-max-full-width" data-src="{{ coll.label | append: '/' | append: image.name }}" alt="{{ image.basename }}" />
				</article>
				{% endfor %}
			</div>
		</div>	
	</div>
</div>