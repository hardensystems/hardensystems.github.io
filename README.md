# Harden Systems — Site Setup

## One-time setup

1. Create a new GitHub repository named exactly: hardensystems.github.io
   (this exact naming makes GitHub Pages host it automatically)
2. Upload every file/folder in this package into that repo, keeping the
   same folder structure (drag-and-drop works in GitHub's web UI —
   just make sure folders like _layouts and _content stay intact).
3. In the repo, go to Settings -> Pages
4. Under "Build and deployment," source should be "Deploy from a branch,"
   branch "main," folder "/ (root)" -- save.
5. Wait 1-2 minutes. Your site will be live at
   https://[your-github-username].github.io
6. To use hardensystems.com instead: in the repo, add a file at the root
   called "CNAME" containing just: hardensystems.com
   Then in Porkbun, point the domain's DNS at GitHub Pages instead of
   forwarding to allmylinks (ask Claude for the exact DNS records when
   you're ready for this step).

## Publishing new content

See CONTENT-TEMPLATE.md for the exact steps and a copy-paste template.
Short version: write the piece, save it in _content/, upload to GitHub,
done. Site rebuilds itself automatically.
