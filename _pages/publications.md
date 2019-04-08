---
layout: page
permalink: /publications/
title: Publications
description: Please take a gander at my publications if you feel so inclined!
years: [2019, 2017, 2016, 2015]
---

<h2>Journal Articles</h2>
{% for y in page.years %}
  <h3 class="year">{{y}}</h3>
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}


