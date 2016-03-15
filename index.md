---
layout: default
title: {{ site.name }}
---

##Welcome to my website
You can download a zip file of codes in my main [github repo](https://github.com/moosekaka/sweepython).

You can download a PDF of my thesis [here]({{ site.github.url }}/thesis/thesis.pdf).

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


