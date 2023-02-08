---
layout: page
title: All Music
permalink: /music/
---

<div>
  <p>All music pages available on this site are listed alphabetically below.
  </p>
  
</div>

<div>

  {% for cat in site.category_list %}
  <h4> {{ cat }} </h4>
  <ul>
    {% for page in site.pages %}
      {% if page.resource == true %}
        {% for pc in page.categories %}
          {% if pc == cat %}
            <li><a href="{{ page.url }}">{{ page.title }}</a></li>
          {% endif %}   <!-- cat-match-p -->
        {% endfor %}  <!-- page-category -->
      {% endif %}   <!-- resource-p -->
    {% endfor %}  <!-- page -->
  </ul>
  {% endfor %}  <!-- cat -->
    
</div>

