---
layout: page
title: About
permalink: /about/
---
<link rel="stylesheet" type="text/css" href="/stylesheets/cards.css">

{% assign authors_by_position = site.authors | sort: "hierarchy" %}
<ul>
  {% for author in authors_by_position %}
    <a class="card" href="{{ author.website }}">
      <img class="avatar" src="{{ author.avatar }}"/>
      <br />
      <h3>{{ author.name }}</h3>
      <h4>{{ author.position }}</h4>
      <h5>{{ author.content | markdownify }}</h5>
    </a>
  {% endfor %}
</ul>
