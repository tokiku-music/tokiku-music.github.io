---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: home
title: Welcome!

popular: "Hustle and Bustle of Ormos"
recent: "Fading Memories"
---
<body>

  <div>
    <p> Feel free to explore as you wish. </p>
  </div>


<!-- display featured songs on home page -->

  <div class="row">
  
    <div class="column">
      <h2> Popular </h2>
      {% for p in site.pages %}
        {% if p.resource == true %}
          {% if p.title == page.popular %}
            <a href="{{ p.url }}"><img alt="{{p.title}}" src="{{p.url}}/{{p.file_name}}.png">
            </a>
          {% endif %}
        {% endif %}
      {% endfor %}
    </div>
    
    <div class="column">
      <h2> Recent </h2>
      {% for p in site.pages %}
        {% if p.resource == true %}
          {% if p.title == page.recent %}
            <a href="{{ p.url }}"><img alt="{{p.title}}" src="{{p.url}}/{{p.file_name}}.png">
            </a>
          {% endif %}
        {% endif %}
      {% endfor %}
    </div>
    
  </div>

    
   
</body>
  
