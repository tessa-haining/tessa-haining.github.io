---
title: "Title of the work"
collection: publications
category: articles
permalink: /research/YYYY-MM-DD-short-slug
excerpt: 'One or two sentences describing the work.'
date: YYYY-MM-DD
venue: 'Journal, conference, or publisher'
paperurl: 'https://example.com/link-to-paper.pdf'
slidesurl: 'https://example.com/link-to-slides.pdf'
bibtexurl: 'https://example.com/link-to-entry.bib'
citation: 'Haining, Tessa. (YYYY). &quot;Title of the work.&quot; <i>Venue</i>. Vol(Issue).'
published: false
---

Copy this file, rename it `YYYY-MM-DD-short-slug.md`, fill in the fields above,
and delete the `published: false` line to make it appear.

`category:` must be one of the four keys defined under `publication_category`
in _config.yml:

  articles    -> "Articles"
  conferences -> "Conference and Workshop Papers"
  essays      -> "Essays"
  inprogress  -> "Works in Progress"

Entries are grouped under those headings on /publications/ and sorted newest
first by `date`. Optional fields (paperurl, slidesurl, bibtexurl, excerpt) can
be deleted if they don't apply — each one only renders a link when present.

Anything written here, below the front matter, becomes the body of the
work's own page, which the title on /publications/ links to. The `citation`
field is appended there automatically in a smaller font.
