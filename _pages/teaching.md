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
  <div class="semester-heading">{{ semester_group.name }}</div>
  {% for course in semester_group.items %}
    {% if forloop.first %}
      <div class="university-name">{{ course.university }}</div>
    {% endif %}
    <div class="course-title">{{ course.title }}</div>
  {% endfor %}
{% endfor %}
