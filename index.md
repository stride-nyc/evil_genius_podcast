---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
title: Welcome To Evil Geniuses
layout: default
---

# Welcome to Evil Geniuses
## A view into the dark underbelly of code

Hosted by Meredith Edwards and Emmanuel Genard.
Each week we break down solutions to code problems,
talking about the decisions that got us where we are.
We reveal our thinking and discuss trade-offs.

<h3 class="no-border dark-red">Evil devs. Evil problems. Evil code<h3>

<ul class="list-style-none">
{% for post in site.posts limit:10 %}
  <li>
    <a href="{{ site.url }}{{ post.url }}" class="black">
      <h3 class="no-border ">
        {{ post.title }}
      </h3>
      <span class="entry-date subtitle"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>
      {% if post.excerpt %}
      <p class="excerpt">{{ post.excerpt }}</p>
      {% endif %}
    </a>
  </li>
{% endfor %}
</ul>
