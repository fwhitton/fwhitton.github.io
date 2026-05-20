---
layout: default
title: Blog
---

# Hedonistic Calculus
Hello and welcome to my blog! This blog is intended as an expository and non-rigorous treatment of some maths problems and topics at ~undergraduate level.

<div style="
  display: grid;
  grid-template-columns: 1fr;
  gap: 25px;
  margin-top: 20px;
">

{% for post in site.posts %}
  <div onclick="window.location.href='{{ post.url }}'" style="
    border: 1px solid #e0e0e0;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
    cursor: pointer;
  "
  onmouseover="this.style.transform='translateY(-5px)'; this.style.boxShadow='0 6px 15px rgba(0,0,0,0.1)';"
  onmouseout="this.style.transform='translateY(0)'; this.style.boxShadow='0 2px 6px rgba(0,0,0,0.05)';">

    {% if post.image %}
      <img src="{{ post.image | relative_url }}" 
           alt="{{ post.title }}"
           style="width:100%; height:180px; object-fit: cover;">
    {% endif %}

    <div style="padding: 15px;">
      <h3 style="margin-top: 0;">
        {{ post.title }}
      </h3>

      <p style="font-size: 0.85em; color: gray;">
    {{ post.date | date: "%Y-%m-%d" }} · 
    {{ post.content | number_of_words | divided_by: 200 }} min read
    </p>

      <p style="margin-bottom: 0;">
        {{ post.excerpt | strip_html | truncate: 120 }}
      </p>
    </div>

  </div>
{% endfor %}

</div>
