# Changelog

The version shows in the footer of the site and beside the title in the editor, so you can always tell which build is live.

Versions step up by 0.1 for a batch of changes, and by 0.0.1 for a small fix. When something changes in a way that would break an older `content.json`, that's a 1.0.

---

## v0.5 — 8 Aug 2026

**Changed**
- Toolset replaced: the sorting quiz is gone, and the tools now drop into the section as physical chips that pile up. Grab and fling them, or shove them around with the cursor. They fall in once per visit, when the section scrolls into view
- Once the pile stops moving, everything glides into a tidy three-column list on its own, so the toolset always ends up readable without anyone doing anything. "Drop them again" replays it
- Reduced-motion visitors get the tidy list immediately, with no physics

## v0.4.1 — 8 Aug 2026

**Fixed**
- Nav links for empty sections are now hidden too. Previously an empty Writing section hid itself but left a dead link in the header

## v0.4 — 8 Aug 2026

**Added**
- Toolset is now a sorting game: pick a tool, choose the discipline it belongs to. Wrong guesses shake the column, right ones slot in. "Show me the answers" and "Just show the list" are always one click away for anyone who'd rather just read it

**Changed**
- Case study intro text now sits under the heading instead of floating off to the right
- Card grid reflows by available width, so a single case study no longer sits in half a row
- The button in the detail panel is now Share, using the phone's share sheet, with copy-to-clipboard as the fallback. Sharing a blog post uses the post's title

## v0.3.1 — 8 Aug 2026

**Fixed**
- Scroll rail stayed on "Writing" while you were reading the contact section. The last section is now selected once the page reaches the bottom, since a short final section never crosses the midpoint of the screen

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
