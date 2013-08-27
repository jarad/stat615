---
layout: page
title: Welcome to STAT 615
tagline: Advanced Bayesian Methods
---
{% include JB/setup %}


<img src="http://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Bayes_icon.svg/200px-Bayes_icon.svg.png" align="right" />
Instructor: [Jarad Niemi](http://jarad.me). This website is designed to hosts video lectures, labs, and post course discussions (questions and answers); see the [Archive](archive.html) page for a complete list. This course meets

- TR 11-12:20 Lagomarcino W262

Here's a sample "posts list".

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

For readings go [here](/schedule/).


