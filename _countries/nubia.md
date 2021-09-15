---
permalink: /combs/nubia/
title: Combs from Nubia
layout: default
label: Nubia
image: "https://media.britishmuseum.org/media/Repository/Documents/2014_11/4_19/0083019e_e6c5_4dbd_a862_a3d9013be010/mid_01188475_001.jpg"
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
