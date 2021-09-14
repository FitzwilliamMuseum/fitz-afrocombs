---
permalink: /combs/ghana/
title: Combs from Ghana
layout: default
label: Ghana
image: https://afrocombs.fitzmuseum.cam.ac.uk/images/combs/Z-35225_VERSO.jpg
---
<div class="container mb-3">
  <div class="row">
  {% for post in site.combs %}
    {% if post.categories contains page.label %}
    <div class="col-md-4 mb-3">
      <div class="card h-100" >
        <a href="{{ post.url }}" class="stretched-link">
          {% include structure/comb-image.html %}
        </a>
        <div class="card-body">
          <h3 class="lead mt-2">
            <a href="{{ post.url }}" class="stretched-link">{{post.title}}</a>
          </h3>
          <p>
            {{ post.institution }}<br/>
            <a href="btn btn-info">{{ post.categories }}</a><br/>
            {% if post.period %}
            {{ post.period }}
            {% endif %}
          </p>
        </div>
      </div>
    </div>
    {% endif %}
  {% endfor %}
  </div>
</div>
