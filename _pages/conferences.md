---
layout: page
permalink: /conferences/
title: conferences 
description: All the conferences where I've been or works with my co-authorship were presented. 
nav: true
---


{% for entry in site.data.conferences %}

{% capture tag_string %}{{ entry[0] }}{% endcapture %}
{% include conference.html tag=tag_string %}

{% endfor %}

