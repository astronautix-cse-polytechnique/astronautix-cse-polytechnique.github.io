---
comments: false
date: 2012-03-07 08:40:21+00:00
layout: page
share: false
meta: false
slug: evenements
title: Événements
excerpt: Les événements proposés par Astronautix
tags: Astronautix, Polytechnique, binet, spatial, centre spatial étudiant, étudiant, événement
---

<div class="tiles">
{% for post in site.categories.event %}
{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->

