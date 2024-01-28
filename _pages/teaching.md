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
  {% assign semester_name, university_name = semester.name | split: ' - ' %}
  <div class="semester-heading">{{ semester_name }} - {{ university_name }}</div>
  <ul class="course-listing">
    {% for course in semester.items %}
      <li>
        <span class="course-code">{{ course.code }}</span>
        <span>{{ course.title }}</span>
        {% if course.comments %}
          <span class="course-comment"> - {{ course.comments }}</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
{% endfor %}

