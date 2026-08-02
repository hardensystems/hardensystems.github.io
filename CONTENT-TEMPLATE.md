# How to add a new piece of content

1. Copy this template.
2. Save it inside the `_content` folder as a new file, e.g. `_content/diy-hair-gel.md`
   (use lowercase, dashes instead of spaces — this becomes the URL)
3. Fill in the front matter (the part between the --- lines) and write the content below it in plain text/Markdown.
4. Upload the file to the `_content` folder in your GitHub repo. The site rebuilds automatically.

-----------------------------------------------------------------
COPY EVERYTHING BELOW THIS LINE INTO YOUR NEW FILE
-----------------------------------------------------------------

---
title: "DIY Hair Gel"
date: 2026-08-02
tags: [diy, recipes]
affiliate_link: "https://amazon.com/your-affiliate-link-here"
affiliate_label: "Get the ingredients"
affiliate_text: "Everything I used for this batch:"
---

Write your post here. This is regular text — talk through the steps,
what you used, what worked. Markdown formatting works too:

- Bullet points like this
- **Bold text**
- [Links like this](https://example.com)

The affiliate box at the bottom of the page is automatic — it pulls from
the affiliate_link, affiliate_label, and affiliate_text fields above.
If you don't need it for a specific post, just delete those three lines
from the front matter and the box won't show up.

TAGS: use any combination of diy, recipes, fitness, finance
(or add a new one — just be consistent with spelling so it groups correctly)
