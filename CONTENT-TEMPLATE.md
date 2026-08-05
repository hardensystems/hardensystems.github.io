# How content gets added to hardensystems.com

This isn't a manual reference — it's a note for future-you. The actual workflow
happens in conversation with Claude, not by editing this file directly.

## The system

1. You film/post a piece of content (usually YouTube).
2. You hand Claude: the link, a title, the date, the real story (what happened,
   what you tried, what worked — a rough transcript or recap is enough), and
   any affiliate/product links.
3. Claude writes it as a proper page: real write-up, embedded video, tags,
   parts/affiliate list if relevant.
4. You paste the file into `_content/` on GitHub, commit.
5. It shows up automatically: homepage "Latest," the archive, and whichever
   topic page(s) match its tag(s).

## Default: full write-up, not a mirror

Most content should be a real page — this is what actually lets Google index
and rank it, not just a link that bounces straight to YouTube. Structure:

---
title: "Title Here"
date: YYYY-MM-DD
tags: [diy]
platform: "YouTube"
video_id: "XXXXXXXXXXX"
---

Real writing here. What happened, what you tried, what fixed it.
Video embeds automatically at the top from video_id.

## Tagging

One tag per piece, almost always. Only add a second tag if the content is
genuinely, substantially about both topics — not just loosely related.
Multiple tags on nearly everything makes topic pages feel repetitive.

## Exception: mirror entries

For quick, low-effort posts with nothing much to say — no write-up, just a
thumbnail and a direct link out. Rare, not the default.

---
title: "Title Here"
date: YYYY-MM-DD
tags: [diy]
external_url: "https://youtube.com/watch?v=XXXXXXXXXXX"
platform: "YouTube"
video_id: "XXXXXXXXXXX"
---

## Non-YouTube platforms (TikTok, LinkedIn, etc.)

No auto-thumbnail available — screenshot the post, upload it to /assets/,
and reference it with a `thumbnail:` field instead of `video_id`.
