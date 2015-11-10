---
layout: archive
permalink: /
title: ""
---
<div class="wrap">

	<a href="/latest/"><h1>Derniers articles</h1></a>
		<div class="tiles">
			{% for post in site.posts limit:4%}
				{% include post-grid.html %}
			{% endfor %}
		</div><!-- /.tiles -->

</div>


<div class="wrap">
	<a href="/event/"><h1>Événements</h1></a>
		<div class="tiles">
			{% for post in site.categories.event limit:4%}
				{% include post-grid.html %}
			{% endfor %}
		</div><!-- /.tiles -->
</div>


<div class="wrap">
	<a href="/miniconf/"><h1>Conférences</h1></a>
	<div class="tiles">
		{% for post in site.categories.miniconf limit:4%}
			{% include post-grid.html %}
		{% endfor %}
	</div><!-- /.tiles -->
</div>