---
layout: page
permalink: /publications/
title: publications
description: 
nav: true
nav_order: 2
---

<div class="publications">
  <h2>Papers</h2>
  {% bibliography --query @article,@inproceedings,@techreport,@unpublished %}
  <h2>Book Chapter</h2>
  {% bibliography --query @inbook,@incollection %}
</div>

