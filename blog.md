---
layout: default
title: Blog
---
Hello and welcome to my blog! This is blog is intended as an expository and non-rigourous treatment of some problems and topics in ~undergraduate maths, hopefully made accessible for anyone with a minimally mathematical background.
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
      ({{ post.date | date: "%Y-%m-%d" }})
    </li>
  {% endfor %}
</ul>
