---
layout: page
title: All Music
permalink: /music/
---

<div>
  <p>This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at <a href="https://jekyllrb.com/">jekyllrb.com</a>.
  </p>
  <p>Songs are listed alphabetically.
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

