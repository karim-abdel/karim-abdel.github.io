---
layout: page
permalink: /teaching/
title: coursework
description: List of my coursework during my academic career
nav: true
nav_order: 6
---

{% assign sorted_courses = site.courses | sort: 'semester_sort' | reverse %}
{% assign courses_by_semester = sorted_courses | group_by: "semester" %}
{% for semester_group in courses_by_semester %}
  <h2 class="semester-heading">{{ semester_group.name }} - {{ semester_group.items.first.university }}</h2>
  <ul class="courses-list">
  {% for course in semester_group.items %}
    <li class="course-title">{{ course.title }}</li>
  {% endfor %}
  </ul>
{% endfor %}
