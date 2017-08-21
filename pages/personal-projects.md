---
layout: page
title: Projects
permalink: /projects/
order: 2
---

Here are a few of my personal projects: <br>

{% assign mypages = site.projects | sort: "order" %}
{% for page in mypages reversed%}
  <hr>
  <div style="height: 4cm">
  <a href="{{ page.url | absolute_url }}">{{ page.title }}</a>
  <a href="{{ page.url | absolute_url }}">
  <img src="{{ site.baseurl }}{{ page.photo }}" alt=" " style="float: right; height: 100%; padding-left: 10px; border-radius: 20px;">
  </a>
  <p>{{ page.about }}</p>
  </div>
{% endfor %}
