---
layout: archive
permalink: /
title: "Astronautix, binet spatial de l'Ecole Polytechnique"
excerpt: Bienvenue sur le site d'Astronautix et du Centre Spatial Étudiant de l'école Polytechnique.
tags: AstronautiX, Polytechnique, Centre spatial étudiant, observation, cubesat, xcubesat, dubiss, association, binet, étudiant
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