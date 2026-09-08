# Iman Jamall — portfolio redesign

Working preview of the imanjamall.com redesign. **Not the live site** — that's still Squarespace at [imanjamall.com](https://www.imanjamall.com), untouched, while this gets built out.

**Preview:** https://iman642.github.io/iman-jamall-portfolio/
(deliberately excluded from search indexing via `robots.txt` until it's ready)

## Status

Actively in progress. Open items — missing images, facts to confirm, sections still being written — are tracked in the working artifact, not in this repo. Ask Claude for the current punch list rather than assuming this repo reflects a finished state.

## Structure

```
index.html        About / home
work.html         Work grid, filterable by tag
work/*.html       Individual case studies
press.html        Education, fellowships, awards, verified press coverage
resume.html       Embeds iman-jamall-cv.pdf
styles.css        Shared design system (color, type, layout tokens)
images/           Real assets pulled from source decks/reports where found
404.html          Custom not-found page
```

## Local development

No build step — it's plain HTML/CSS. To preview locally with working relative paths:

```bash
cd site-preview
python3 -m http.server 4173
# open http://localhost:4173
```

## Deploying changes

Every push to `main` auto-publishes via GitHub Pages within ~30–60 seconds:

```bash
git add -A
git commit -m "describe the change"
git push
```

## Migration plan

When this is ready to become the real site: point imanjamall.com's DNS at GitHub Pages (or move to Cloudflare Pages for parity with other projects), remove `robots.txt`'s disallow, and retire the Squarespace subscription. Not yet — this is a working preview until then.
