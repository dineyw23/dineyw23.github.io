---
layout: page
title: Projects
---

---

<div id="projects">
    {% for project in site.data.projects %}
        <div class="project">
        <h1> {{ project.name }} </h1>
  </div>
  {% endfor %}
</div>
