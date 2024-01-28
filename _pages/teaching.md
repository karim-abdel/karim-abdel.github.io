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
  <h2 class="semester-heading">{{ semester_group.name }} - {{ semester_group.items.first.university }}</h2>
  <ul class="courses-list">
  {% for course in semester_group.items %}
    <li class="course-title">{{ course.title }}</li>
  {% endfor %}
  </ul>
{% endfor %}