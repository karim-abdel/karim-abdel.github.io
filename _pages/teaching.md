---
layout: page
permalink: /teaching/
title: Coursework
description: Detailed descriptions of my coursework during my academic career
nav: true
nav_order: 6
---

{% assign courses_by_semester = site.courses | group_by: "semester" %}
{% for semester_group in courses_by_semester %}
  <h2 class="semester-heading">{{ semester_group.name }}</h2>
  {% assign courses = semester_group.items | sort: 'title' %}
  {% for course in courses %}
    {% if forloop.first %}
      <h3 class="university-name">{{ course.university }}</h3>
    {% endif %}
    <div class="course-title">{{ course.title }}</div>
  {% endfor %}
{% endfor %}