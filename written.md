---
layout: default
title: Written work
permalink: /written/
---

{% for post in site.written reversed %}
<div class="card col-md-12 mb-1">
    <div class="card-body">
      {% if post.thumbnail %}
      <div class="float-right">
        <div class="news-thumb p-2 m-2">
          <img src="{{ post.thumbnail }}" class="img img-responsive " />
        </div>
      </div>
      {% endif %}
        <h3><a href="{{site.baseurl}}{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{ post.content }}</p>
    </div>
</div>
{% endfor %}
