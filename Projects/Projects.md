---
layout: page
title: Projects
---

---

<div id="projects">
    {% for project in site.data.projects %}
        <div class="project">
        <h1> {{ project.name }} 
        <span class="separator" style="font-size: 20px">|</span>
        <span style="font-size: 20px">
        <span style="font-weight: normal">
        <span style="color:#4C4C4C">{{ project.tagline }}</span></span></span></h1>
      <div class="meta">
                <span class="time" style="font-weight: bold"><span style="color:#333333">{{ project.time }}</span></span>
                <span class="toolstack">| <span style="color:#0087FF">toolstack:</span></span> {{ project.tools | join: ", " }}
            </div>
      {% if project.description }}
      <div class="description">{{ project.description | markdownify }}</div>
      {% endif %}   
      {% if project.url or project.github %}
                {% if project.url %}
                    <a href="{{ project.url }}" class="btn btn-md btn-default" target="_blank"><i class="fa fa-link fa-fw"></i>view online</a>
                {% endif %}
                {% if project.github %}
                    <a href="https://github.com/{{ project.github.url }}" class="btn btn-md btn-default" target="_blank"><i class="fa fa-github fa-fw"></i>view on GitHub</a>
                {% endif %}

            {% endif %}      

  </div>
  {% endfor %}
</div>
