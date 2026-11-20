# ezquiaga.github.io — Claude Instructions

## Site overview
Personal academic website for Jose Maria Ezquiaga (Associate Professor, Niels Bohr Institute).
Built with the Plain-Academic template (Bootstrap 3.3.6), hosted on GitHub Pages.

Pages: index.html, research.html, cv.html, group.html, talks.html, teaching.html, outreach.html, events.html, news.html, joinus.html

## Workflow
**FUNDAMENTAL: Always ask for explicit permission before committing or pushing.** Never commit or push automatically, even after an edit is made.

When the user approves a commit, use:
  git add <file> && git commit -m "<message>" && git push origin master

## news.html
CoG-style image cards, 2 per row, grouped by year (`<h3 class="news-year">YEAR</h3>` + `<div class="row news-row">`), **newest first** by date.
- New items go as the first card inside the relevant year's `news-row`. If the year doesn't exist yet, add a new `<h3>` + `news-row` block at the top.
- Card format:
  ```html
  <div class="col-sm-6 news-card" words="add, your, keywords, here">
    <a href="URL" target="_blank"><img src="images/news/<slug>.jpg" alt="Title" draggable="false"></a>
    <div class="news-date">Nov. 3, 2026</div>
    <a class="news-title" href="URL" target="_blank">Title</a>
    <div class="news-extra">Optional secondary links/text</div>
  </div>
  ```
- **Link:** the card links to the external page (CoG, KU, journal, ...). If there is no external page, the card has no link: drop the `<a>` around the image and use `<span class="news-title">Title</span>`. Do not create local news pages unless the user asks for one.
- **Date:** use the most precise date available (`Mon. D, YYYY`), in this priority: date on the linked article > date stated in the item itself > date of the commit that added the item (`git log -S"<text>" --reverse -- news.html`).
- **Image:** 880×600 JPG, quality ~82, saved to `images/news/<slug>.jpg` (center-crop; posters/portrait images are letterboxed on a blurred copy). Take it from the external link (header/og:image of the article, or the matching poster in `images/posters/web/` for events). **If an image cannot be obtained directly from the external link, always ask the user for one** — never substitute a stock or topic image. Until it arrives, a plain grey 880×600 `images/news/placeholder.jpg` can be used for layout checks, but don't commit it. Originals the user provides go in `images/news/originals/` (gitignored).

## group.html
Sections in order:
1. **NBI LIGO Group** — current members. Format: `Name, Role`
2. **Visiting fellows** — longer stays (weeks to months). Format: `Name, Role, Institution, Month–Month Year`
3. **Short-term visitors** — brief visits. Format: `Name, Role, Institution, Month Year`. Newest first.
4. **Past members** — former group members, with thesis links where applicable.

If the user does not provide the role or institution for a visitor, search the web to find it before asking.

## events.html
Gallery of posters of events Jose has organized, 3 per row, **newest first**.
- The user drops original posters (PDF/PNG/JPG) in `images/posters/`. These are **not published** (`.gitignore` excludes everything in `images/posters/` except `web/`).
- For each new poster, make a web copy: 700px tall JPG, quality ~82, saved to `images/posters/web/<name>.jpg` (PDFs: render the first page, e.g. with `sips -s format png`, then resize with PIL).
- Add a `<figure>` block in the correct date position, copying the format of existing ones: poster wrapped in `<a href="EVENT_URL" target="_blank">`, `draggable="false"` on the `<img>`, and a `<figcaption>` with `<b>Title</b><br/>Place, Month Year`.
- Take title, place and date from the poster itself. For the link, prefer the Center of Gravity features page (`https://the-center-of-gravity.com/features/...`) when one exists; otherwise the official event website.
- Check the layout with a headless Chrome screenshot before asking to commit.

## Center of Gravity news check
At the start of every conversation about updating the website, fetch https://the-center-of-gravity.com to check for recent news that could be relevant (new group members, awards, papers, events, etc.) and proactively suggest additions.

## External resources
- You have permission to fetch content from https://the-center-of-gravity.com to retrieve news, thesis, or event details.
- You have permission to fetch content from https://strong-gr.com to retrieve event or project details.
- You have permission to fetch content from https://nbi.ku.dk to retrieve news, event, or project details.

## HTML style
- Keep the `class="paper" words="add, your, keywords, here"` attribute on all `<li>` elements.
- Do not add comments or change surrounding structure when making small edits.
