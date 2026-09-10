---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
{% comment %} The download link below appears automatically once you upload files/cv.pdf {% endcomment %}
{% assign cv_pdf = site.static_files | where: "path", "/files/cv.pdf" | first %}
{% if cv_pdf %}
[Download full CV (PDF)]({{ base_path }}/files/cv.pdf)
{% endif %}

Education
======
* PhD in Modern Thought and Literature, Stanford University, in progress
* MPhil in Modern Languages (with distinction), University of Oxford, [year]. Rhodes Scholar
* [Degree], Chemistry and Comparative Literature, Harvard University, [year]

Research experience
======
* Computational biology research at MIT, Harvard, and the Dana-Farber Cancer Institute [add roles and years]

{% comment %} The sections below fill themselves from _publications, _talks, and _teaching, and stay hidden while those folders are empty. {% endcomment %}
{% if site.publications.size > 0 %}
Research
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
{% endif %}

{% if site.talks.size > 0 %}
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
{% endif %}

{% if site.teaching.size > 0 %}
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
{% endif %}
