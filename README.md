# Your academic website

This repository holds your website. It is **private**, so no one else can see its files, and nothing is published as a website until you follow **Going public** at the bottom of this page.

## How to edit anything

Every change works the same way:

1. Click a file to open it.
2. Click the **pencil icon** at the top right of the file.
3. Make your change. The **Preview** tab shows how text will look.
4. Click **Commit changes…**, type a short note (for example, "update bio"), and click **Commit changes**.

Committing is saving. Each file's **History** keeps every earlier version, so nothing you change is lost.

- **Add a file:** open the folder, then **Add file → Create new file**. Typing a `/` in the name creates a folder.
- **Upload a PDF or photo:** open the folder, then **Add file → Upload files**. A file with the same name replaces the old one.
- **Delete a file:** open it, click **⋯** at the top right, then **Delete file**.

## What lives where

| To change | Edit |
|---|---|
| Your name, sidebar bio, email, profile links (Google Scholar, ORCID, and so on) | `_config.yml`, top section |
| Homepage text | `_pages/about.md` |
| The menu across the top | `_data/navigation.yml` |
| The CV page | `_pages/cv.md` |
| Downloadable CV | upload a PDF named `cv.pdf` into `files/`; a download link appears on the CV page by itself |
| Your photo | upload a headshot named `profile.png` into `images/` (for a .jpg, upload it and change `avatar` in `_config.yml` to its file name) |
| Research entries | one file per item in `_publications/` |
| Talks | one file per talk in `_talks/` |
| Teaching | one file per course in `_teaching/` |
| Color scheme | `site_theme` in `_config.yml`: `default`, `air`, `sunrise`, `mint`, `dirt`, or `contrast` |

The top section of each entry file (between the `---` lines) is structured data the site reads. Keep the quotation marks and colons as they are, and it will work.

## Adding a research entry

In `_publications/`, create a file named with the date first and no spaces, such as `2026-10-15-short-title.md`, and paste this in:

```yaml
---
title: "Title of the Piece"
collection: publications
category: inprogress
permalink: /publication/2026-10-15-short-title
date: 2026-10-15
venue: "Name of Journal, Conference, or Workshop"
status: "Under review"
excerpt: "One or two sentences on the question it asks. With Co-author Name."
citation: 'Tessa Haining. (2026). "Title of the Piece." <i>Venue</i>.'
paperurl: "https://link-to-a-pdf-or-preprint"
---

Optional longer description, shown on the entry's own page.
```

- `category` picks the section of the Research page: `articles`, `conferences` (conference and workshop papers), `essays`, or `inprogress` (works in progress). An entry without a category won't appear. Section names are set under `publication_category` in `_config.yml`.
- `status` is for anything not yet published: `Forthcoming`, `Under review`, or `In progress`. The site then shows the status instead of "Published in". Leave the line out for published work.
- For anonymous review, leave out `venue` and keep `status: "Under review"`, so reviewers can't match the paper to you.
- `permalink` should match the file name, without `.md`.
- Delete any line you don't need, such as `citation` or `paperurl`.
- Check with your collaborators before listing joint work that isn't published yet.

## Adding a talk

In `_talks/`, create a file such as `2027-02-20-short-title.md`:

```yaml
---
title: "Title of the Talk"
collection: talks
type: "Conference presentation"
permalink: /talks/2027-02-20-short-title
venue: "Name of Conference"
date: 2027-02-20
location: "City, State"
---

Optional abstract.
```

When you add or change a talk, an automated job called **Scrape Talk Locations** may run and add a commit of its own; it updates the template's optional talk map. To switch it off: **Actions** tab → **Scrape Talk Locations** → **⋯** → **Disable workflow**.

## Adding teaching

In `_teaching/`, create a file such as `2026-fall-course-name.md`:

```yaml
---
title: "Course Title"
collection: teaching
type: "Teaching assistant"
permalink: /teaching/2026-fall-course-name
venue: "Stanford University, Program Name"
date: 2026-09-22
location: "Stanford, CA"
---
```

## Previewing while private (optional)

GitHub won't publish a private repository, but Codespaces can show you a private preview in your browser:

1. On this page, click the green **Code** button → **Codespaces** tab → **Create codespace on master**.
2. Wait while it sets up. The first time can take several minutes.
3. When a message says an application on port 4000 is available, click **Open in Browser**. If you miss it, open the **Ports** tab and click the globe icon next to 4000.

Only you can see the preview. Keep making your edits on github.com: changes typed inside the codespace aren't saved to the repository unless you commit them there. A codespace shows the site as it was when you created it, so for a fresh look, delete the old one at [github.com/codespaces](https://github.com/codespaces) and create a new one. Personal accounts include about 60 hours of free use a month at the default size, and an idle codespace stops itself after 30 minutes.

## Going public

**Before you publish:**

- [ ] Your name near the top of `_config.yml` appears the way you want it.
- [ ] No `[bracketed]` placeholders are left in `_pages/cv.md`.
- [ ] Your photo has replaced `images/profile.png`.
- [ ] The menu in `_data/navigation.yml` links only to pages that have something on them.
- [ ] The template's leftover demo pages are deleted from `_pages/`: `markdown.md`, `non-menu-page.md`, `archive-layout-with-content.md`, `cv-json.md`, and `terms.md` (a privacy policy you didn't write).
- [ ] The sample files are deleted from `files/`: `paper1.pdf`, `paper2.pdf`, `paper3.pdf`, `slides1.pdf`, `slides2.pdf`, `slides3.pdf`, `bibtex1.bib`.
- [ ] Collaborators have agreed to any joint work you list.

**Then choose a route.**

**Route A: make the repository public (free).**

1. **Settings → General**, scroll to **Danger Zone**, and choose **Change repository visibility → Public**.
2. **Settings → Pages**: under *Build and deployment*, set Source to **Deploy from a branch**, choose branch **master** and folder **/ (root)**, and click **Save**.
3. After a few minutes the site is live at `https://tessa-haining.github.io`. The Pages settings screen shows the link once it's up.

This also makes the repository's files and complete edit history public, including anything you drafted and later deleted.

**Route B: keep the repository private (free for students).** With GitHub Pro, a private repository can publish a public site, and verified students get Pro free through GitHub Education at [education.github.com](https://education.github.com) (approval can take a few days). Once Pro is active, do only step 2 above. The site is public; the repository and its history stay private.

**To take the site down later:** Settings → Pages, click **⋯** next to "Your site is live at", then **Unpublish site**.

**If the site stops updating:** open the **Actions** tab. A red ✗ next to *pages build and deployment* means the last change has an error, usually a missing quotation mark or colon in `_config.yml` or in an entry's top section. Click the run to see which file, then fix it or restore the earlier version from the file's History.
