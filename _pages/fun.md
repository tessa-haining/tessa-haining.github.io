---
layout: archive
title: "Fun"
permalink: /fun/
author_profile: true
---

As a former varsity rower, I've been privy to almost a decade of breathtaking sunrises and sunsets, from Boston to Oxford and now California, where I study. They really, truly, never get old.

I've done my best to document the ones I can; here are some of my favorites down below.

{% include base_path %}
{% assign photos = site.data.fun.photos %}
{% if photos and photos.size > 0 %}
<div class="photo-grid">
  {% for photo in photos %}
  <figure style="--ar: {{ photo.width | times: 1.0 | divided_by: photo.height }}">
    <img src="{{ base_path }}/images/fun/{{ photo.file }}"
         width="{{ photo.width }}" height="{{ photo.height }}"
         alt="{{ photo.alt | default: 'Sunrise or sunset photograph' }}"
         loading="lazy" decoding="async">
    <figcaption>{{ photo.caption }}</figcaption>
  </figure>
  {% endfor %}
</div>
{% endif %}
