---
permalink: /combs/rwanda/
title: Combs from Rwanda
layout: default
label: Rwanda
image: https://static.portal.maa.cam.ac.uk/portal-assets/media/library_images/web/662121_1948.2338_A_001.png
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
