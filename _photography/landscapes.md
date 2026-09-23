---
layout: page
title: Landscapes
description: A short line describing this album — edit me.
img: assets/img/1.jpg # album cover thumbnail — replace with one of your own photos
importance: 1
category: landscapes
---

<!--
  ======================= HOW TO USE THIS ALBUM =======================
  1. Put your photo files in:  assets/img/photography/landscapes/
     (create that folder; any .jpg/.png works).
  2. For each photo, copy a {% raw %}{% include figure.liquid ... %}{% endraw %} line below and
     change `path=` to point at your file, e.g.
        path="assets/img/photography/landscapes/sunset.jpg"
  3. Put images side-by-side by adding more <div class="col-sm"> blocks
     inside a <div class="row">. One row = one horizontal strip.
  4. The placeholder photos below use the theme's sample images
     (assets/img/1.jpg ...). Swap them for yours, then delete this comment.
  =====================================================================
-->

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="replace with your caption" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2.jpg" title="replace with your caption" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A caption for the row above — edit or delete me.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/3.jpg" title="replace with your caption" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
