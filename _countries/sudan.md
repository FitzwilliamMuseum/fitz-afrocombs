---
permalink: /combs/sudan/
title: Combs from Sudan
layout: default
label: Sudan
image: https://media.britishmuseum.org/media/Repository/Documents/2014_11/4_19/b264cc65_d1ac_424a_8f03_a3d9013e8ab2/small_01189026_001.jpg

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
          <a href="btn btn-info">{{ post.categories }}</a>
        </div>
      </div>
    </div>
    {% endif %}
  {% endfor %}
  </div>
</div>
