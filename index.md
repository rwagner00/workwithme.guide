---
layout: default
title: Home
---

## Summary

[workwithme.guide](./) is a quick prototype for hosting Work With Me Guides. It's built using [GitHub Pages](https://pages.github.com/), [Jekyll](https://jekyllrb.com/), and [minimal theme](https://github.com/pages-themes/minimal).

[Kuan Luo wrote a great post](https://www.cockroachlabs.com/blog/how-to-work-with-me/) about Work With Me Guides, if you're interested.

## Work With Me Guides

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

## Adding Your Work With Me Guide

If you'd like your Work With Me Guide here, see [the documentation](./adding-your-wwm-guide.html).
