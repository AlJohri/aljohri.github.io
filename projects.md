---
layout: page
title: Projects
permalink: /projects/
---

<ul class="post-list">
  <!-- sort projects https://github.com/jekyll/jekyll/issues/2515#issuecomment-46107601 -->
  {% for project in site.projects %}
    <li>

      <h3>{{project.title}}</h3>

      <ul class="project-links">
        {% if project.live %}<li><a href="{{project.live}}">Live</a></li>{% endif %}
        {% if project.source %}<li><a href="{{project.source}}">Source</a></li>{% endif %}
      </ul>

      {% if project.picture %}
  	  <div style="max-height: 400px; overflow: hidden;">
  	    <img src="{{project.picture}}" alt=""/>
  	  </div>
      {% endif %}

      {% if project.embed %}
        {{ project.embed }}
      {% endif %}

      <article class="post-content">
        {% if project.description %}
          {{ project.description | markdownify }}
        {% endif %}
      </article>

      <a href="{{project.url}}">Read More</a>

    </li>
  {% endfor %}
</ul>


