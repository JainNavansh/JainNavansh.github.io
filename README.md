# Navansh Jain — Technical Artist portfolio

Two files matter to you:

| File | What it is |
|---|---|
| `index.html` | The site. You never need to open this. |
| `content.json` | All your content. Every word, project and link. |
| `editor.html` | A visual editor for `content.json`. This is where you work. |

---

## Adding a project (the whole workflow)

1. Open `editor.html` — double-click it, or visit `yoursite.com/editor.html`.
2. Click **Case studies** in the sidebar, then the **+ Add case study** button at the top of the list.
3. Fill in the fields. It saves a draft in your browser as you type.
4. Click **Preview site** to see it live in a new tab before publishing.
5. Click **Download content.json**.
6. Replace the old `content.json` on your host with the downloaded one.

Step 6 on GitHub: open your repo → click `content.json` → the pencil icon → delete everything → paste the new file's contents → **Commit changes**. Live in about a minute. On Netlify, drag the whole folder onto the deploys page again.

Same flow for a blog post, a job, a skill group, or changing your name — it's all in the sidebar.

## What the editor gives you

- **+ Add** button pinned to the top of every list, plus one at the bottom — new entries open expanded with the cursor in the first field
- Add, delete and reorder entries with the ↑ ↓ buttons
- Live previews for images, videos and date ranges — you see it before you publish
- Drafts survive closing the tab — nothing is lost if you get interrupted
- **Preview site** renders your unsaved draft in a new tab, so you check before you publish. The badge in the corner tells you which draft you're looking at.
- **Import file** loads a `content.json` from anywhere, in case you edit on two machines
- **Discard draft** throws away local changes and reloads what's actually published

The editor is a plain page with no login. Anyone who finds the URL can *look* at it, but they can't change your site — publishing means downloading a file and uploading it yourself. If you'd rather it not be public at all, just don't upload `editor.html` to your host and run it locally instead.

## Formatting inside text fields

- `<b>like this</b>` bolds a phrase inside any paragraph or bullet
- The **About paragraphs** field takes one paragraph per line
- Bullet fields take one bullet per line
- Blog post bodies use `<p>…</p>` for paragraphs and `<h3>…</h3>` for subheadings

## Videos

Every project, blog post, toolset group and job has a **YouTube video** field. Paste any YouTube link — `watch?v=`, `youtu.be`, `shorts`, or embed — and it plays inline on the page. The editor shows the video's thumbnail as soon as it recognises the link, so you know straight away that it worked.

Nothing loads from YouTube until someone actually clicks play. Until then it's just a thumbnail, which keeps the page fast and means no YouTube cookies are set on visitors who never watch.

If a project has a video but no cover image, the card uses the video thumbnail with a play badge.

## Images

Put your files in an `images/` folder next to `index.html`, then type the path (`images/your-shot.jpg`) into any image field. The editor previews it immediately.

Image fields exist on:

- **Projects** — cover image, plus a gallery
- **Blog posts** — cover image, plus a gallery
- **Toolset groups** — one image under the list
- **Experience** — a small company logo beside the role

The **Gallery** on projects and posts takes any mix of images and videos, each with an optional caption. Add rows with the dropdown set to Image or Video.

Leave a project's cover empty and the generated pattern comes back — nothing is ever a broken image.

## Dates

Experience entries use month and year dropdowns rather than free text. Tick **Still working here** and the end date is replaced with "Present". The editor shows a live preview of exactly how the date will read.

---

## Putting it online

**GitHub Pages** — create a public repo, upload all files, then Settings → Pages → Deploy from branch → `main` / root.

**Netlify or Cloudflare Pages** — drag the folder onto netlify.com/drop. Free URL and HTTPS, custom domain supported.

### A note on opening files directly

If you double-click `editor.html` to open it, the browser treats it as a local file and blocks some features:

- **Autosave stops.** The editor tells you so in an orange banner. Everything still works — just click **Download content.json** before closing the tab.
- **`index.html` opened directly won't reflect `content.json` edits.** It falls back to a copy baked in at build time.

**Preview site still works correctly in both cases** — the preview window asks the editor for your current draft directly, rather than going through storage.

To get autosave back, serve the folder instead of double-clicking. In a terminal, from this folder:

```
python3 -m http.server
```

Then open `http://localhost:8000/editor.html`. Everything behaves exactly as it will once published.

## Already handled

Responsive to small phones · shareable deep links (`#work/asset-pipeline`) · native share sheet on mobile · keyboard navigation and focus rings · `prefers-reduced-motion` respected · no tracking, no cookies, no commercial anything.
