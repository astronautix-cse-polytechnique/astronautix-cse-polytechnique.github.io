---
layout: archive
permalink: /
title: ""
---
<div class="wrap well">

	<a href="/latest/"><h2>Derniers articles</h2></a>
		<div class="tiles">
			{% for post in site.posts limit:4%}
				{% include post-grid.html %}
			{% endfor %}
		</div><!-- /.tiles -->

</div>


<div class="wrap well">
	<a href="/event/"><h2>Événements</h2></a>
		<div class="tiles">
			{% for post in site.categories.event limit:4%}
				{% include post-grid.html %}
			{% endfor %}
		</div><!-- /.tiles -->
</div>


<div class="wrap well">
	<a href="/miniconf/"><h2>Conférences</h2></a>
	<div class="tiles">
		{% for post in site.categories.miniconf limit:4%}
			{% include post-grid.html %}
		{% endfor %}
	</div><!-- /.tiles -->
</div>