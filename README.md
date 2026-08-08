# Navansh Jain — Technical Artist portfolio

Current version: **v0.7** — see `CHANGELOG.md` for what changed.

| File | What it is |
|---|---|
| `index.html` | The site. You never need to open this. |
| `content.json` | All your content. Every word, project and link. |
| `editor.html` | A visual editor for `content.json`. This is where you work. |
| `CHANGELOG.md` | What changed in each version. Not uploaded to your site. |

---

## Adding a project (the whole workflow)

1. Open `editor.html` — double-click it, or run it locally.
2. Click **Case studies** in the sidebar, then **+ Add case study** at the top of the list.
3. Fill in the fields. It saves a draft in your browser as you type.
4. Click **Preview site** to see it live in a new tab before publishing.
5. Click **Download content.json**.
6. Replace `content.json` on your host with the downloaded one.

Step 6 on GitHub: open your repo → click `content.json` → the pencil icon → select all → paste the new contents → **Commit changes**. Live in about a minute.

## Covers

Every case study can have, in order of preference:

1. **A cover image** — `images/your-shot.jpg`. Always the best option.
2. **A YouTube video** — the thumbnail is used, with a play badge.
3. **A generated cover** — pick a style and accent colour in the editor:
   - **Title card** — the project name in large type on a dark gradient. Best when you have no screenshot yet.
   - **Flow lines**, **Blocks**, **Dot field** — abstract patterns, seeded from the project slug so they stay the same between visits.
   - **Auto** — one of the three patterns, chosen for you.

## Videos

Every project, blog post, toolset group and job has a YouTube field. Paste any link — `watch?v=`, `youtu.be`, `shorts`, or embed. Nothing loads from YouTube until someone clicks play.

## Images

Put files in an `images/` folder next to `index.html`, then type the path into any image field. Image fields exist on: profile picture and cover banner, project covers and galleries, blog posts, toolset groups, and company logos in experience.

Keep them under about 500KB each so the page stays quick on phones.

## Contact links

Type a plain email address or web address and the link is built for you. On desktop the email button copies your address (mailto often does nothing there); on phones it opens the mail app.

## Formatting inside text fields

- `<b>like this</b>` bolds a phrase in any paragraph or bullet
- About paragraphs: one paragraph per line
- Bullet fields: one bullet per line
- Blog bodies use `<p>…</p>` and `<h3>…</h3>`

## Putting it online

**GitHub Pages** — public repo, upload the files, Settings → Pages → Deploy from branch → `main` / root.

**Netlify or Cloudflare Pages** — drag the folder onto netlify.com/drop.

### Opening files directly

Double-clicking `editor.html` means the browser blocks autosave (an orange banner tells you) and `index.html` won't reflect `content.json` edits. **Preview site still works.** To get autosave back, run `python3 -m http.server` in the folder and open `localhost:8000/editor.html`.

## Already handled

Responsive · shareable deep links (`#work/triyuga`) · native share sheet · keyboard navigation · `prefers-reduced-motion` respected · no tracking, no cookies, nothing commercial.
