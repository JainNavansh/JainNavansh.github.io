# Navansh Jain — Technical Artist portfolio

Current version: **v0.7.5** — see `CHANGELOG.md` for what changed.

| File | What it is |
|---|---|
| `index.html` | The site. You never need to open this. |
| `content.json` | All your content. Every word, project and link. |
| `editor.html` | A visual editor for `content.json`. This is where you work. Keep it off your host. |
| `CHANGELOG.md` | What changed in each version. Not needed on your site. |

---

## The workflow

1. Open `editor.html` — double-click it, or serve it locally (see below).
2. Edit. It saves a draft in your browser as you type.
3. Click **Preview site** to check it in a new tab.
4. Click **Download content.json**.
5. Replace `content.json` on your host with the downloaded file.

On GitHub: open your repo → click `content.json` → the pencil icon → select all → paste the new contents → **Commit changes**. Live in about a minute.

## Filling in your content

Sidebar sections, in the order worth doing them:

- **Name & intro** — name, role, the cycling focus line, hero paragraph, profile picture, cover image, about text
- **Hero numbers** — the four figures under the cover. They count up from zero when scrolled into view
- **Quick facts** — the list beside your about text
- **Case studies** — the main event. See below
- **Experience** — job timeline with month/year pickers
- **Toolset** — groups of tools. These become the chips in the drop-and-tidy toy
- **Blog posts** — optional. The section hides itself if empty
- **Contact links** — type a plain email or web address; the link is built for you

## Writing a case study

Each one wants: a one-line summary, the problem, what you did, the outcome, and optionally what you'd take forward. The problem and outcome are what people actually read — what was slow or broken before, and what changed. The clever middle section is for those who ask.

Keep slugs lowercase with dashes (`silent-escape`, not `Silent Escape`) — they become your shareable links, like `#work/silent-escape`.

An empty case study reads worse than a shorter list. Better to publish one good one than four stubs.

## Covers

In order of preference:

1. **A cover image** — `images/your-shot.jpg`. Always best.
2. **A YouTube video** — its thumbnail is used, with a play badge.
3. **A generated cover** — pick a style and accent colour in the editor:
   - **Title card** — the project name in large type on a dark gradient. Best when you have no screenshot yet.
   - **Flow lines**, **Blocks**, **Dot field** — abstract patterns, seeded from the slug so they stay the same between visits.
   - **Auto** — one of the three, chosen for you.

## Videos

Projects, blog posts, toolset groups and jobs all take a YouTube link — `watch?v=`, `youtu.be`, `shorts` or embed. Nothing loads from YouTube until someone clicks play, so the page stays fast and no cookies are set on visitors who never watch.

## Images

Put files in an `images/` folder next to `index.html`, then type the path into any image field. Fields exist on: profile picture, cover banner, project covers and galleries, blog posts, toolset groups, and company logos.

Keep them under about 500KB each. Cover banner around 2000x600, profile square, project shots around 1600 wide.

## Formatting inside text fields

- `<b>like this</b>` bolds a phrase in any paragraph or bullet
- About paragraphs: one paragraph per line
- Bullet fields: one bullet per line
- Blog bodies use `<p>...</p>` for paragraphs and `<h3>...</h3>` for subheadings

## Putting it online

**GitHub Pages** — public repo, upload the files, Settings then Pages, Deploy from branch, `main` / root.

**Netlify or Cloudflare Pages** — drag the folder onto netlify.com/drop, or connect the repo for automatic deploys on every commit.

Don't upload `editor.html`. It's your back office and it doesn't need to be public. Nobody could change your site through it, but there's no reason to display it.

### Opening files directly

Double-clicking `editor.html` means the browser blocks autosave — an orange banner tells you, and you should download before closing the tab. `index.html` opened directly also won't reflect `content.json` edits. **Preview site works either way.**

To get autosave back, from this folder run:

```
python3 -m http.server
```

Then open `http://localhost:8000/editor.html`.

## Already handled

Responsive to small phones, shareable deep links (`#work/triyuga`), native share sheet on mobile, email copies on desktop where mailto often fails, keyboard navigation and focus rings, `prefers-reduced-motion` respected throughout, no tracking, no cookies, nothing commercial.
