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
	<a href="/events/"><h1>Événements</h1></a>
		<div class="tiles">
			{% for post in site.categories.Evenement limit:4%}
				{% include post-grid.html %}
			{% endfor %}
		</div><!-- /.tiles -->
</div>


<div class="wrap">
	<a href="/miniconfs/"><h1>Conférences</h1></a>
	<div class="tiles">
		{% for post in site.categories.Miniconf limit:4%}
			{% include post-grid.html %}
		{% endfor %}
	</div><!-- /.tiles -->
</div>