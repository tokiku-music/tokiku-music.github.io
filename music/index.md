---
layout: page
title: All Music
permalink: /music/
---

<div>
  <p>All music pages available on this site are listed alphabetically by category below.
  </p>
  
</div>

<div>

  {% assign today = site.time %}
  {% assign sortedCats = site.category_list | sort %}
  {% assign sortedPages = site.pages | sort: 'title' | where_exp: "item", "item.date <= today" %}
  {% for cat in sortedCats %}
    <details>
    <summary class="level_one"> {{ cat }} </summary>
    <ul id="music-list" style="list-style-type:circle;">
      {% for page in sortedPages %}
        {% if page.resource == true %}
            {% for pc in page.categories %}
              {% if pc == cat %}
                <li><a href="{{ page.url }}">{{ page.title }}</a></li>
              {% endif %}   <!-- cat-match-p -->
            {% endfor %}  <!-- page-category -->
        {% endif %}   <!-- resource-p -->
      {% endfor %}  <!-- page -->
    </ul>
    </details>
  {% endfor %}  <!-- cat -->
    
</div>


