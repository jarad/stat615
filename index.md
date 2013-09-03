---
layout: page
title: Welcome to STAT 615
tagline: Advanced Bayesian Methods
---
{% include JB/setup %}


<img src="http://upload.wikimedia.org/wikipedia/commons/thumb/e/ed/Bayes_icon.svg/200px-Bayes_icon.svg.png" align="right" />
Instructor: [Jarad Niemi](http://jarad.me). This website is designed to hosts course materials for [STAT 615 - Advanced Bayesian Methods](http://catalog.iastate.edu/showcourse/?code=STAT-615&edition=2013-14) at [Iowa State University](http://www.iastate.edu). This course meets

- TR 11-12:20 Lagomarcino W262

Recent posts for material relevant to STAT 615:

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

### Course links

- [Readings](readings.html)
- [Homework](homework.html)



