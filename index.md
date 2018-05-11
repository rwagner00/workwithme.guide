---
layout: default
---

{% for p in site.pages %}
    {% if p.categories contains 'profile' %}
## [{{ p.full_name }}]({{ p.url }})
      {% if p.picture %}
![{{ p.full_name }}]({{ p.url | append: "/" | append: p.picture | absolute_url }})
      {% else %} 
![{{ p.full_name }}](https://upload.wikimedia.org/wikipedia/commons/7/7c/Profile_avatar_placeholder_large.png)
      {% endif %}
   {% endif %}
{% endfor %}
