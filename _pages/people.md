---
title: "Researchers"
permalink: "/people/"
layout: article
---

<style>

.headshot {
  max-height: 300px;
  max-width: 300px;
  border-radius: 50%;
}

</style>

<h1>{{ page.title }}</h1>

## Faculty

{% assign faculty = site.data.people.faculty | sort: "lastname" %}

<ul>
{% for person in faculty %}

  <li>{{ person.name }}</li>

  {% if person.photo %}
  <img class="headshot" src="{{ person.photo }}">
  {% endif %}

{% endfor %}
</ul>

## Graduate Students

{% assign current_students = site.data.people.students | where: "type", "current" | sort: "join_year" %}

<ul>
{% for student in current_students %}

  <li>{{ student.name }}</li>
  {% if student.photo %}
  <img class="headshot" src="{{ student.photo }}">
  {% endif %}

{% endfor %}
</ul>

## Alumni

{% assign alumni = site.data.people.students | where: "type", "alumni" | sort: "graduation_year" | reverse %}

<ul>
{% for student in alumni %}
  <li>{{ student.name }}</li>
{% endfor %}
</ul>

<!--
* Haley MacLeod (PhD, 2018 — Facebook)
* Shayan Khokar (BS, 2018 — Amazon)
* Anna Baglione (MS, 2018 — U. of Virginia)

* Leslie S. Liu (Post-Doctoral Fellow, 2017 – Motorola)

* Shuo Yang (PhD, 2017 – Amobee)
* Phillip Odom (PhD, 2017 – Georgia Tech)
* Majdah Alshehri (PhD Student)
* Annu Prabhakar (PhD Student)
* Christopher Schaefbauer (PhD, 2016 – Amazon)
* Swaminathan Ananthanarayan (PhD, 2015 – U. of Oldenburg)
* Danish U. Khan (PhD, 2013 – Informatica)

* Kimberly Oakes (MS, 2015)

* Allison Brown (PhD Student)
* Halley Profita (PhD Student)
* Gerald Pulver (PhD Student)

* Tuong An (Amy) Le (BS, 2014)
* Noelle Beaujon (BS Student)
* Mackenzie Miller (BS Student)
* Maryam Gooyabadi (BS, 2010)
* Alice Chien (BS, 2015 – Deloitte Digital)
* Miranda Sheh (BS, 2015 – Ambi Labs)
* Nate Lapinski (BS, 2014 – SpotXchange)
* Sara Zhang (BS Student)
* Erin Leonhard (BS Student)
-->
