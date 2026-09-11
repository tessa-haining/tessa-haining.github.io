---
title: "Entry template"
collection: teaching
published: false
---

Copy this file, rename it `YYYY-term-short-slug.md`, and replace its front
matter with the block below, filled in.

IMPORTANT: `date:` must be a real date, e.g. `2026-01-06`. Jekyll parses the
date of every file in this folder *before* it checks `published:`, so a
placeholder like `YYYY-MM-DD` aborts the whole build with an
`InvalidDateError` even on a file that is not published. That is why the
example below sits in a code block rather than in this file's front matter.

```yaml
title: "Title of the course or teaching role"
collection: teaching
type: "Undergraduate course"
permalink: /teaching/2026-spring-short-slug
venue: "Institution, Department"
date: 2026-01-06
location: "City, Country"
```

`type:` is free text and displays as written — e.g. "Undergraduate course",
"Graduate seminar", "Guest lecture", "Workshop".

`date:` is used for sorting only (newest first); for a term rather than a
single day, use the first day of that term.

Anything below the front matter becomes the body of the entry's own page,
which the title on /teaching/ links to.
