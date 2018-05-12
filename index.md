---
layout: default
---

## Summary

[workwithme.guide](./) is a quick prototype for housing Work With Me documents so that they are publicly available and easy to review changes over time. This is accomplished by leveraging [GitHub Pages](https://pages.github.com/), based on the [Jekyll](https://jekyllrb.com/) [minimal theme](https://github.com/pages-themes/minimal).

*See [Kuan Luo’s great post](https://www.cockroachlabs.com/blog/how-to-work-with-me/) if you’re new to Work With Me docs.*

## Adding Your Work With Me Document

1. Fork [this project](https://github.com/abloomston/workwithme.guide) on GitHub
2. Copy [the template directory](https://github.com/abloomston/workwithme.guide/tree/master/template) to a new top-level sub-directory. This sub-directory name will be your link on `https://workwithme.guide/sub-directory-name`.
3. Modify `index.md`, optionally adding a profile picture to the sub-directory.
4. Commit your changes.
5. Make a [Pull Request](https://help.github.com/articles/about-pull-requests/). This is how you will make changes to your Work With Me Document (for now--this is a prototype).
6. Once I merge your Pull Request your Work With Me Document will be available at `https://workwithme.guide/sub-directory-name`.


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
