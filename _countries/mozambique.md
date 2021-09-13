---
permalink: /combs/mozambique/
title: Combs from Mozambique
layout: default
label: Mozambique
---
<div class="container mb-3">
  <div class="row">
  {% for post in site.combs %}
    {% if post.categories contains page.label %}
    <div class="col-md-4 mb-3">
      <div class="card h-100" >
        <a href="{{ post.url }}" class="stretched-link">
          <img class="img-fluid" src="{{post.preview}}" alt="{{ post.title }}" />
        </a>
        <div class="card-body">
          <h3 class="lead mt-2">
            <a href="{{ post.url }}" class="stretched-link">{{post.title}}</a>
          </h3>
          <a href="btn btn-info">{{ post.categories }}</a>
        </div>
      </div>
    </div>
    {% endif %}
  {% endfor %}
  </div>
</div>
