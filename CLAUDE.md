# ezquiaga.github.io — Claude Instructions

## Site overview
Personal academic website for Jose Maria Ezquiaga (Associate Professor, Niels Bohr Institute).
Built with the Plain-Academic template (Bootstrap 3.3.6), hosted on GitHub Pages.

Pages: index.html, research.html, cv.html, group.html, talks.html, teaching.html, outreach.html, news.html, joinus.html

## Workflow
**FUNDAMENTAL: Always ask for explicit permission before committing or pushing.** Never commit or push automatically, even after an edit is made.

When the user approves a commit, use:
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

If the user does not provide the role or institution for a visitor, search the web to find it before asking.

## Center of Gravity news check
At the start of every conversation about updating the website, fetch https://the-center-of-gravity.com to check for recent news that could be relevant (new group members, awards, papers, events, etc.) and proactively suggest additions.

## External resources
- You have permission to fetch content from https://the-center-of-gravity.com to retrieve news, thesis, or event details.
- You have permission to fetch content from https://strong-gr.com to retrieve event or project details.
- You have permission to fetch content from https://nbi.ku.dk to retrieve news, event, or project details.

## HTML style
- Keep the `class="paper" words="add, your, keywords, here"` attribute on all `<li>` elements.
- Do not add comments or change surrounding structure when making small edits.
