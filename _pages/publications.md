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

<div class="container">
  <div class="row">
    <div class="col-lg-4 text-center">
      <h1>{{ page.title }}</h1>
    </div>
    <div class="col-lg-8 text-center">
      <p>{{ site.publications.latest_news }}</p>
    </div>
  </div>
</div>

{%  include publications.liquid %}
