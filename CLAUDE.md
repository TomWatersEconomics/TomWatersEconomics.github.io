# Tom Waters – academic website

Static site hosted on GitHub Pages (TomWatersEconomics.github.io). Plain HTML/CSS, no build step, no framework. Keep it that way.

## Workflow
- Claude edits and commits; Tom clicks "Push origin" in GitHub Desktop. (Cowork blocks git push from Claude's side, so don't try.)
- Before the first commit in a session, request delete permission for this folder (git creates and deletes lock files).
- Commit as: `git -c user.name=TomWatersEconomics -c user.email=88095619+TomWatersEconomics@users.noreply.github.com commit -m "..."`
- Repo has `core.autocrlf=true` (Windows checkout, CRLF in working tree). Stage specific files, never `git add -A` blindly; check `git status` is clean apart from intended changes.
- Run `git fetch` first; if behind origin, ask Tom to click "Pull origin" in GitHub Desktop before editing.
- After committing, tell Tom which file(s) changed and to push.

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
