---
layout: default
---

## Summary

[workwithme.guide](./) is a quick prototype for housing Work With Me documents so that they are publicly available and easy to review changes over time. This is accomplished by leveraging [GitHub Pages](https://pages.github.com/), based on the [Jekyll](https://jekyllrb.com/) [minimal theme](https://github.com/pages-themes/minimal).

## Work With Me Documents

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
