---
layout: page
permalink: /teaching/
title: Coursework
description: Detailed descriptions of my coursework during my academic career
nav: true
nav_order: 6
---

{% assign courses_by_semester = site.courses | group_by: "semester" %}
{% for semester in courses_by_semester %}
  <h2>{{ semester.name }}</h2>
  <ul>
    {% for course in semester.items %}
      <li>
        <span>{{ course.code }}</span>
        <a href="{{ course.url }}">{{ course.title }}</a>
        {% if course.comments %}
          <span> - {{ course.comments }}</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
{% endfor %}

