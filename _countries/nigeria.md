---
permalink: /combs/nigeria/
title: Combs from Nigeria
layout: default
label: Nigeria
image: https://static.portal.maa.cam.ac.uk/portal-assets/media/library_images/thumbnail/585702_2012.19_001.png
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
