---
title: "Entry template"
collection: publications
published: false
---

Copy this file, rename it `YYYY-MM-DD-short-slug.md`, and replace its front
matter with the block below, filled in.

IMPORTANT: `date:` must be a real date, e.g. `2026-05-14`. Jekyll parses the
date of every file in this folder *before* it checks `published:`, so a
placeholder like `YYYY-MM-DD` aborts the whole build with an
`InvalidDateError` even on a file that is not published. That is why the
example below sits in a code block rather than in this file's front matter.

```yaml
title: "Title of the work"
collection: publications
category: articles
permalink: /research/2026-05-14-short-slug
excerpt: 'One or two sentences describing the work.'
date: 2026-05-14
venue: 'Journal, conference, or publisher'
paperurl: 'https://example.com/link-to-paper.pdf'
slidesurl: 'https://example.com/link-to-slides.pdf'
bibtexurl: 'https://example.com/link-to-entry.bib'
citation: 'Haining, Tessa. (2026). &quot;Title of the work.&quot; <i>Venue</i>. Vol(Issue).'
```

`category:` must be one of the four keys defined under `publication_category`
in _config.yml:

  articles    -> "Articles"
  conferences -> "Conference and Workshop Papers"
  essays      -> "Essays"
  inprogress  -> "Works in Progress"

Entries are grouped under those headings on /research/ and sorted newest first
by `date`. Optional fields (paperurl, slidesurl, bibtexurl, excerpt) can be
omitted — each renders a link only when present.

Anything below the front matter becomes the body of the work's own page, which
the title on /research/ links to. The `citation` field is appended there
automatically in a smaller font.
