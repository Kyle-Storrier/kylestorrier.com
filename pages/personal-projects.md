---
layout: page
title: Projects
permalink: /projects/
order: 2
---

Here are a few personal and team projects I have worked on: <br>

{% assign mypages = site.projects | sort: "order" %}
{% for page in mypages reversed%}
  <hr style="padding-top: 1px; padding-bottom: 1px; clear: both;">
  <div style="height: auto; padding-top: 1px; padding-bottom: 1px;">
  <a href="{{ page.url | absolute_url }}">{{ page.title }}</a>
  <a href="{{ page.url | absolute_url }}">
  <img src="{{ site.baseurl }}{{ page.photo }}" alt=" " style="float: right; height: 4cm; padding-left: 10px; padding-bottom: 5px; padding-top: 5px;border-radius: 20px;">
  </a>
  <p style="padding-top: 1px; padding-bottom: 1px;">{{ page.about }}</p>
  </div>
{% endfor %}
