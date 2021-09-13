---
layout: default
permalink: /combs/
title: Explore combs
---
To explore the Afro combs included in this project, you can navigate several ways:

* by country of origin below
* by a [map interface](/combs/map)
* by a [timeline](/combs/timeline) (links to be enabled shortly)

<div class="container mb-3">
  <div class="row">
  {% assign rows = site.countries.size | divided_by: 2.0 | ceil %}
  {% for i in (1..rows) %}
  {% assign offset = forloop.index0 | times: 2 %}
  {% assign sorted = site.countries | sort:"order" %}
      {% for author in sorted limit:2 offset:offset %}
      <div class="col-md-4 mb-3">
        <div class="card h-100" >
          <a href="{{ author.url }}" class="stretched-link">
            <img class="img-fluid" src="{{author.image}}" alt="{{ author.title }}" />
          </a>
          <div class="card-body">
            <h3 class="lead mt-2">
              <a href="{{ author.url }}" class="stretched-link">{{author.title}}</a>
            </h3>
          </div>
        </div>
      </div>
      {% endfor %}
    {% endfor %}
  </div>
</div>
