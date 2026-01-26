---
title: Projects
layout: collection
collection: projects
permalink: /projects/
author_profile: true
classes: wide
---

This section contains selected academic and applied data science projects focused on public policy. 

{% assign featured_projects = site.projects | where: "featured", true %}
{% assign regular_projects = site.projects | where_exp: "p", "p.featured != true" %}

<h2>Featured Projects</h2>
<ul>
  {% for project in featured_projects %}
    <li><a href="{{ project.url }}">{{ project.title }}</a></li>
  {% endfor %}
</ul>

<h2>All Projects</h2>
<ul>
  {% for project in regular_projects %}
    <li><a href="{{ project.url }}">{{ project.title }}</a></li>
  {% endfor %}
</ul>
