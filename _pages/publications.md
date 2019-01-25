---
title: "Publications"
permalink: "/publications/"
layout: article
comment: >-
  This is somewhat experimental, not sure how the final product should
  look so I'll try a few things out --Alexander
---

<style>
  .pub {
    text-decoration: underline
  }
</style>

<h1>{{ page.title }}</h1>

<ul>
{% for people in site.data.publications %}

  {% assign entry = people[1] %}
  <li><a href="{{ entry["uri"] }}">{{ entry["name"] }}</a></li>

  <ul>
  {% for publication in entry.publications %}

    <li>
    {{ publication.authors | join: ", " }}. {{ publication.year }}.

    {% if publication.url %}
      <a class="pub" href="{{ publication.url }}">"{{ publication.title }}"</a>.
    {% else %}
      "{{ publication.title }}".
    {% endif %}

    {% if publication.bibtex %}
      <span data-toggle="tooltip" data-placement="bottom" title="{{ publication.bibtex }}">{{ publication.venue }}</span>
    {% else %}
      {{ publication.venue }}
    {% endif %}

    </li>

  {% endfor %}
  </ul>

{% endfor %}
</ul>

<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js"></script>

<script>
  $(function () {
    $('[data-toggle="tooltip"]').tooltip()
  })
</script>
