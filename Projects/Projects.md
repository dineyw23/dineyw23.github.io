---
layout: page
title: Projects
comments: true
permalink: proj
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
                <span class="toolstack">| <span style="color:#ff7476">toolstack:</span></span> {{ project.tools | join: ", " }}
            </div>
      {% if project.description %}
      <div class="description">{{ project.description | markdownify}}</div>
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
  <br> 
 <hr />
  {% endfor %}
  <div class="disqus">
  <p></p>
  <p></p>
  <h3 align="middle"> Want to share your thoughts?</h3>
  <p></p>
  <p></p>
 </style>
  {% if page.comments  %}
<div id="disqus_thread"></div>
<script>
    /**
     *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
     *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables
     */

//        var disqus_developer = 1;    
/*    var disqus_config = function () {
        this.page.url = "{{ site.url }}"  // Replace PAGE_URL with your page's canonical URL variable
        this.page.identifier = '/proj'; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
        var disqus_developer = 1;    
};*/
  
    (function() {  // DON'T EDIT BELOW THIS LINE
        var d = document, s = d.createElement('script');
        
        s.src = '//dineywankhede.disqus.com/embed.js';
        
        s.setAttribute('data-timestamp', +new Date());
        (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript" rel="nofollow">comments powered by Disqus.</a></noscript>  


  {% endif %}
  </div>

</div>
