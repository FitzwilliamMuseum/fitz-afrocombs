---
permalink: /combs/egypt/
title: Combs from Egypt
layout: default
label: Egypt
image: "https://media.britishmuseum.org/media/Repository/Documents/2014_11/4_19/ce82969f_d82b_4ab6_a3d0_a3d9013dc08b/small_01188846_001.jpg"
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
