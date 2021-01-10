---
layout: page
permalink: /teaching/
title: teaching 
description: ALL IN RUSSIAN. Not delivering regular courses, but supervising a lot of students.
nav: true
years: [2020, 2019, 2018, 2017, 2016, 2015]
---

## Supervised students
      
{% for y in page.years %}
  <h2 class="year">{{y}}</h2>
<p>  
  {% for entry in site.data.students %}{% if entry[1].year == y %}
    {% capture thesis_path %}/assets/thesis/{{ entry[0] }}-thesis.pdf{% endcapture %}
    {% capture pres_path %}/assets/thesis/{{ entry[0] }}-presentation.pdf{% endcapture %}
    {% assign thesis = site.static_files | where: "path", thesis_path | first %}
    {% assign pres = site.static_files | where: "path", pres_path | first %}

[<b>{{ entry[1].degree }}</b>] <b>{{ entry[1].student }}</b>. {{ entry[1].title }}. {{ entry[1].type }}. {{ entry[1].year }}.
[{{ entry[1].supervisors }}]
{% if thesis %}<a href="{{ site.baseurl }}{{ thesis_path }}">[thesis]</a>{% endif %}
{% if pres %}<a href="{{ site.baseurl }}{{ pres_path }}">[presentation]</a>{% endif %}

  {% if true %}{% endif %}
<br/>
  {% endif %}{% endfor %}
</p>  
{% endfor %}

