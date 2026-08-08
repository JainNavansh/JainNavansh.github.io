# Changelog

The version shows in the footer of the site and beside the title in the editor, so you can always tell which build is live.

Versions step up by 0.1 for a batch of changes, and by 0.0.1 for a small fix. When something changes in a way that would break an older `content.json`, that's a 1.0.

---

## v0.7.3 — 8 Aug 2026

**Changed**
- The page was locked to 1180px, so on a 1920px screen a third of the display was empty margin. The shell now grows to 1560px, giving about 1470px of content instead of 1120px, and case studies fit four across on a wide monitor
- Side padding and section spacing now scale with the viewport rather than sitting at fixed values, so the page breathes proportionally instead of getting relatively tighter as screens get bigger
- The hero graph takes a slightly larger share of the row and is a little less letterboxed
- Prose keeps its own maximum width as the shell widens, so lines never get uncomfortably long to read

## v0.7.2 — 8 Aug 2026

**Changed**
- The toolset now resolves into something clearly structured. The playground grid fades away, a card appears behind each group, and the chips shed their pill outlines to become plain list rows with an accent marker
- The bin shrinks to fit once tidied, instead of leaving empty space below the list
- Four groups now lay out as a 2×2 grid rather than three across with one stranded underneath

## v0.7.1 — 8 Aug 2026

**Fixed**
- Hero numbers never appeared. The editor saves them as key/value pairs but the site was reading a different pair of field names, so every entry looked blank and the strip hid itself. The site now accepts either naming
- Experience dates showed only the start year when the end date was left empty. An incomplete range now falls back to whatever was typed by hand
- Project slugs containing spaces broke their shareable links. Links are now encoded and decoded properly

## v0.7 — 8 Aug 2026

**Added**
- Cover style picker on every case study. Choose **Title card** (the project name set in large type on a dark gradient), **Flow lines**, **Blocks**, **Dot field**, or Auto, plus an accent colour. The editor previews your choice as you change it
- Covers are no longer left to chance — Auto is now opt-in rather than the only behaviour

## v0.6.3 — 8 Aug 2026

**Fixed**
- Blank hero numbers rendered as empty boxes with dividers. Empty rows are now skipped, the strip hides itself entirely if none are filled in, and the columns adapt to however many you have

## v0.6.2 — 8 Aug 2026

**Fixed**
- The Focus line clipped its own text. Its height was set in `em`, which resolved against the inherited body size rather than the much larger display size, leaving the box about half as tall as the words. It now sizes from the same font, with headroom for descenders
- More breathing room between the hand-drawn underline and the Focus line
- Long focus phrases now truncate rather than overflowing on narrow screens

## v0.6.1 — 8 Aug 2026

**Fixed**
- The Email button did nothing on desktop machines with no mail client configured. On desktop it now copies the address and confirms which one it copied. On phones and tablets it still opens the mail app, since mailto works reliably there

## v0.6 — 8 Aug 2026

**Changed**
- Hero rebuilt. The role is bigger and tighter, with a hand-drawn underline that draws itself under the last word
- The specialty is no longer a large block of grey caps competing with the title. It's now a single "Focus" line that cycles through your specialty phrases, one at a time, in accent blue
- The opening paragraph is larger, and the hero elements fade up in sequence rather than all appearing at once
- All motion is skipped for visitors who prefer reduced motion

## v0.5.3 — 8 Aug 2026

**Fixed**
- Case study cards with less text showed a white gap above the cover image. Cards are buttons, and buttons centre their contents vertically, so shorter cards floated their content to the middle of the stretched row. Cards are now flex columns anchored to the top

## v0.5.2 — 8 Aug 2026

**Fixed**
- Job title and company ran together on one line in the experience section. They now stack, with the company on its own line beneath the role
- The mint timeline dot now marks whichever roles are current, rather than always the first entry in the list

## v0.5.1 — 8 Aug 2026

**Fixed**
- Once the toolset has tidied itself, clicking or dragging a chip no longer re-drops the pile. The list stays put, and only the "Drop them again" button replays it. Chips also stop showing a grab cursor once they're settled

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
