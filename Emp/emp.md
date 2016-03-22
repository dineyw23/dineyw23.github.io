---
layout: page
title: Employment
permalink: emp

---

---

<div id="employment">
    {% for emp in site.data.emps %}
        <div class="emps">
        <h1> {{ emp.name }} 
        <span class="separator" style="font-size: 20px">|</span>
        <span style="font-size: 20px">
        <span style="font-weight: normal">
        <span style="color:#ff7476">{{ emp.tagline }}</span></span></span></h1>
      <div class="meta">
            <span class="time" style="font-weight: bold">
            <span style="color:#333333">{{ emp.time1 }} - {{emp.time2 }}
            </span></span>
      </div>
      {% if emp.description %}
      <div class="description">{{ emp.description | markdownify}}</div>
      {% endif %}   
      {% if emp.url %}      
      <a href="{{ emp.url }}" class="btn btn-md btn-default" target="_blank">               <i class="fa fa-link fa-fw"></i>view online</a>
      {% endif %}      
    </div>
    <br> 
  <hr />
    {% endfor %}
</div>
