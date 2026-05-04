# ezquiaga.github.io — Claude Instructions

## Site overview
Personal academic website for Jose Maria Ezquiaga (Associate Professor, Niels Bohr Institute).
Built with the Plain-Academic template (Bootstrap 3.3.6), hosted on GitHub Pages.

Pages: index.html, research.html, cv.html, group.html, talks.html, teaching.html, outreach.html, news.html, joinus.html

## Workflow
After the user approves an edit, immediately commit and push to GitHub without asking:
  git add <file> && git commit -m "<message>" && git push origin master

## news.html
- News items are ordered **newest first** within each year block.
- New items go as the first `<li>` inside the relevant year's `<ul>`.
- Use this format for each item:
  `<li class="paper" words="add, your, keywords, here">Text with optional <a href="URL">link</a></li>`
- If the year doesn't exist yet, add a new `<strong>YEAR</strong><br/><ul>...</ul>` block at the top.

## group.html
Sections in order:
1. **NBI LIGO Group** — current members. Format: `Name, Role`
2. **Visiting fellows** — longer stays (weeks to months). Format: `Name, Role, Institution, Month–Month Year`
3. **Short-term visitors** — brief visits. Format: `Name, Role, Institution, Month Year`. Newest first.
4. **Past members** — former group members, with thesis links where applicable.

## HTML style
- Keep the `class="paper" words="add, your, keywords, here"` attribute on all `<li>` elements.
- Do not add comments or change surrounding structure when making small edits.
