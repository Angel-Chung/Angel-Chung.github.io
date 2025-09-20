---

layout: default         # keep the site header/nav
title: CV
permalink: /cv/
nav: true
nav_order: 2
description: My CV
cv_pdf: AngelCV.pdf
classes: wide           # ←← THIS lifts the 820-px limit
---
<!-- centred pill button -->
<div class="d-flex justify-content-center my-2">
  <a href="{{ page.cv_pdf | prepend: 'assets/pdf/' | relative_url }}"
     target="_blank" rel="noopener"
     class="btn btn-outline-primary rounded-pill shadow-sm d-inline-flex align-items-center gap-1 px-3 py-2">
    <i class="fa-solid fa-file-arrow-down"></i>
    Download Full CV
  </a>
</div>

<!-- LARGE, centred preview -->
<div class="d-flex justify-content-center">
  <object data="{{ page.cv_pdf | prepend: 'assets/pdf/' | relative_url }}"
          type="application/pdf"
          style="
            width: 94vw;          /* almost edge-to-edge */
            max-width: 1500px;    /* but don’t go crazy on ultrawides */
            height: 92vh;         /* tall, yet leaves room for navbar */
            border: 1px solid #e5e5e5;
            border-radius: .5rem;
            box-shadow: 0 0 8px rgba(0,0,0,.06);
          ">
    <p class="text-center">
      Your browser can’t display PDFs.
      <a href="{{ page.cv_pdf | prepend: 'assets/pdf/' | relative_url }}">
        Download the file instead.
      </a>
    </p>
  </object>
</div>
