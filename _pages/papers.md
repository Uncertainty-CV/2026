---
layout: default
permalink: /papers/
title: Accepted Papers
---

# Accepted Full Papers 

<ul>
{% assign sortedPapers = site.data.papers | sort: 'title' %}
{% for item in sortedPapers %}
{% if item.type == "full" %}
  <li><strong>{{ item.title }}</strong>
  {% if item.oral %}
  <em>(Oral)</em>
  {% endif %}
  <br/>
  <small><i>{{ item.authors }}</i></small></li>
{% endif %}
{% endfor %}
</ul>

# Accepted Extended Abstracts

<ul>
{% for item in sortedPapers %}
{% if item.type == "abstract" %}
  <li><strong>{{ item.title }}</strong><br/>
  <small><i>{{ item.authors }}</i></small></li>
{% endif %}
{% endfor %}
</ul>

# Accepted Posters

<ul>
{% for item in sortedPapers %}
{% if item.type == "poster" %}
  <li><strong>{{ item.title }}</strong><br/>
  <small><i>{{ item.authors }}</i></small></li>
{% endif %}
{% endfor %}
</ul>
