---
layout: default
title: Home
---

## Summary

[workwithme.guide](./) is a quick prototype for hosting Work With Me Guides. This is accomplished by leveraging [GitHub Pages](https://pages.github.com/), [Jekyll](https://jekyllrb.com/), and [minimal theme](https://github.com/pages-themes/minimal).

[Kuan Luo wrote a great post](https://www.cockroachlabs.com/blog/how-to-work-with-me/) about Work With Me Guides, if you're interested.

## Adding Your Work With Me Guide

1. Fork [workwithme.guide-myguide](https://github.com/abloomston/workwithme.guide-myguide) on GitHub.
2. Modify `index.md`, optionally adding a profile picture to the top level directory.
3. Fork [this project]({{ site.github.repository_url }}) on GitHub.
4. Clone your fork. In your local sandbox run `git submodule add -b master https://github.com/USERNAME/workwithme.guide-myguide.git WWM_LINK` where `USERNAME` is your GitHub username and `WWM_LINK` is the link you'd like at `workwithme.guide/WWM_LINK`.
5. Make a [Pull Request](https://help.github.com/articles/about-pull-requests/). This is how you will make changes to your Work With Me Guide (for now--this is a prototype).
6. Once I merge your Pull Request your Work With Me Guide will be available at `workwithme.guide/WWM_LINK`.


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
