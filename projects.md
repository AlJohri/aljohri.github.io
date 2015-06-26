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

      <a href="{{project.live}}">Live</a> |
      <a href="{{project.source}}">Source</a>

  	  <div style="max-height: 400px; overflow: hidden;">
  	    <img src="{{project.picture}}" alt=""/>
  	  </div>

      <article class="post-content">
        {{ project.description | markdownify }}
      </article>

      <a href="{{project.url}}">Read More</a>

    </li>
  {% endfor %}
</ul>


