---
layout: page
permalink: /grants/
title: Гранты 
#description: Was working only with Russian grant agencies. 
---

### Руководитель

{% for entry in site.data.grants %}
{% if entry[1].role == 'Руководитель' %}

{% capture tag_string %}{{ entry[0] }}{% endcapture %}
{% include grant.html tag=tag_string %}

{% endif %}
{% endfor %}

### Участник

{% for entry in site.data.grants %}
{% if entry[1].role != 'Руководитель' %}

{% capture tag_string %}{{ entry[0] }}{% endcapture %}
{% include grant.html tag=tag_string %}

{% endif %}
{% endfor %}
