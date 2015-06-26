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

      <article class="post-content">
        {{ project.content }}
      </article>

    </li>
  {% endfor %}
</ul>


