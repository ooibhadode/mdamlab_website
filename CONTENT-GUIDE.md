# Updating the website

Everything below can be done in the browser on GitHub: open the file, click the pencil icon (**Edit**), make the change, then click **Commit changes**. The live site updates a minute or two later.

To upload an image, open the folder it belongs in (for example `assets/images/people/`) and choose **Add file → Upload files**.

> **Tip:** YAML files (`.yml`) depend on indentation. Copy an existing entry and edit it, keep the same spacing, and use spaces rather than tabs. If you break a file, the build fails and the live site stays as it was. You'll see a red ✗ next to the commit; fix the file and commit again.

---

## Add a news item

Create a new file in `_posts/` named `YYYY-MM-DD-short-title.md`, for example `2026-11-20-new-paper-in-addma.md`:

```markdown
---
title: "New paper in Additive Manufacturing"
image: /assets/images/news/addma-2026.jpg      # optional
image_alt: "Short description of the photo"     # optional, also used as the caption
---

The first paragraph is used as the summary on the News and Home pages.

Further paragraphs appear only on the full news page. You can use **bold**,
*italics*, [links](https://example.com) and lists.
```

Upload photos to `assets/images/news/`. Use real photos of the team and the work wherever you can, about 1600 px wide.

## Add or update a person

Edit `_data/team.yml`. Copy an existing person block and change the details:

```yaml
  - name: Jane Doe
    group: grad              # pi | postdoc | visiting | grad | undergrad | alumni
    role: PhD Student
    focus: Topology optimization for heat exchangers
    photo: doe.jpg           # in assets/images/people/; leave out to show initials
    linkedin: https://www.linkedin.com/in/...
    scholar: https://scholar.google.com/citations?user=...
```

Portraits look best as JPGs at **480 × 552 px**, with the face in the upper half.

**When someone graduates or leaves**, change `group:` to `alumni` and set `role:` to something like `MSc 2026 · now at Company X`.

## Add a publication

Edit `_data/publications.yml` and add the new entry at the **top** of the right list (`journal`, `conference`, `books`, `chapters` or `patents`):

```yaml
  - title: Title of the paper
    authors: A. Author, B. Author, O. Ibhadode
    venue: Journal Name
    details: "12, 100345"      # volume, pages/article number (optional)
    year: 2026
    doi: 10.1016/j.xxxx.2026.100345
```

Use `doi:` when there is one; otherwise use `url:`. The page groups entries by year automatically.

## Software, teaching, partners, funding

These follow the same pattern in `_data/software.yml`, `_data/teaching.yml`, `_data/partners.yml` and `_data/funding.yml`. Each file has comments at the top explaining its fields.

For teaching, move a course from `current:` to `previous:` when the term ends.

## Change the menu

Edit `_data/navigation.yml`. Entries with `external: true` open in a new tab and show a small ↗ arrow, as the **Employees** link to the intranet does.

## Research page

`research.html` is ordinary HTML. Each theme is a `<section class="topic">` with its text and a set of `<figure>` elements. To add a figure, copy an existing `<figure>…</figure>` block, upload the image to `assets/images/research/`, and change the file name and caption. Give a short citation in the caption when a figure comes from a paper.
