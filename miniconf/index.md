---
comments: false
date: 2012-03-07 08:40:21+00:00
layout: page
share: false
slug: confs
title: Conférences
---

<div class="tiles">
{% for post in site.categories.miniconf %}
{% include post-grid.html %}
{% endfor %}
</div><!-- /.tiles -->
