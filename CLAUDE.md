# Tom Waters – academic website

Static site hosted on GitHub Pages (TomWatersEconomics.github.io). Plain HTML/CSS, no build step, no framework. Keep it that way.

## Workflow
- Claude edits files in this folder only. Tom reviews, commits and pushes with GitHub Desktop.
- Do not run git commands (no commit, push, stash, checkout).
- After editing, give Tom a short summary of what changed and in which file(s).

## Files
- `index.html` – Research page: intro, contact links, then papers in sections: Working papers, Work in progress, Published papers, Book chapters and invited papers, Resting papers.
- `policy.html` – Policy page: IFS reports grouped by category (each `<h3 class="group">` with an id, listed in the `<nav class="toc">`), then "Selected policy engagement" (evidence to committees; ongoing advisory roles).
- `style.css` – all styling. `cv.pdf`, `photo.jpg`, `favicon.svg` – assets.

## Conventions
- British English, except paper titles and journal names exactly as published.
- Papers: copy an existing `<article class="paper">` block. Fields: year, title, authors as "with A. Surname and B. Surname" (omit if sole-authored), venue in `<p class="venue">` with journal in `<i>`, link button(s) ("Published version", "IFS working paper", "NBER working paper"), abstract in the hidden `<div class="abstract">` with an "Abstract" toggle button. Newest first within each section.
- When a working paper is published, move it to Published papers and update venue and link.
- Policy page: copy an existing `<article class="entry">` block. Reports only (not comments or press releases). Newest first within each group. Engagement entries have a `<p class="meta">` line (body, month year).
- Use typographic quotes/dashes (’ – ) consistent with existing text.
- Update the footer "Last updated <Month Year>" on any page you change.
- Never invent abstracts, coauthors, venues or links: ask Tom, or leave a clear TODO and say so.
