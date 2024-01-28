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
  {% assign first_course = semester_group.items | first %}
  <h2 class="semester-heading">{{ semester_group.name }} - {{ first_course.university }}</h2>
  {% for course in semester_group.items %}
    <p class="course-title">{{ course.title }}</p>
  {% endfor %}
{% endfor %}
