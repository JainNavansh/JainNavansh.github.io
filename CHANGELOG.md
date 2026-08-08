# Changelog

The version shows in the footer of the site and beside the title in the editor, so you can always tell which build is live.

Versions step up by 0.1 for a batch of changes, and by 0.0.1 for a small fix. When something changes in a way that would break an older `content.json`, that's a 1.0.

---

## v0.3 — 8 Aug 2026

**Added**
- Profile picture and cover image, both editable under **Name & intro**
- Scroll rail down the right with section labels, plus a progress bar across the top
- Hero numbers count up when they scroll into view
- Editable footer note, now reading "Designed and built with AI assistance"
- Version stamps in the site footer, the editor, and `content.json`

**Changed**
- Graph labels moved outside the nodes, so long words like "Experience" can no longer crop. The centre node measures your name and resizes to fit
- Graph nodes animate outward on load, drift with scroll, and one pulses until you interact — so it reads as something you can touch
- Experience is now a real timeline: a vertical line with a dot per role, mint for current, indigo for expanded

**Fixed**
- Contact links: type a plain email and the `mailto:` link is built for you; bare web addresses get `https://`. The editor previews the resolved link as you type

## v0.2 — 8 Aug 2026

**Added**
- YouTube video on projects, posts, toolset groups and jobs, playing inline. Nothing loads from YouTube until play is clicked
- Images across all content, plus a mixed image/video gallery on projects and posts
- Month and year pickers for experience dates, with a "Still working here" option
- Prominent **+ Add** buttons at the top of every list, with counts and empty states

**Fixed**
- Preview now receives the draft directly from the editor window, so it works when opening files locally
- Editor no longer fails to load when the browser blocks local storage
- Nested gallery buttons no longer created stray case studies

## v0.1 — 8 Aug 2026

First build. Node-graph hero, case studies with deep links, experience, toolset, blog, share button, and the `content.json` + `editor.html` split.
