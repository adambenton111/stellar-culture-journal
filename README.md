# Stellar Culture Journal 2027 — Go Deeper

Companion landing page for the Stellar Senior Living Culture Journal. Each week's QR code links to this page with an anchor (`#w2`, `#w15`, etc.) so team members can access videos, articles, and resources related to that week's value.

## Quick Start

### Option A: GitHub Pages (easiest)
1. Push this repo to GitHub
2. Go to **Settings → Pages → Source → Deploy from a branch → main**
3. Your site will be live at `https://[your-username].github.io/stellar-culture-journal/`
4. To use a custom domain (e.g., `stellarliving.com/journal`), see [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

### Option B: Drop on any web server
Copy `index.html` to your web server. That's it — it's a single static file with no dependencies or build step.

### Option C: Subdirectory on stellarliving.com
If your main site runs on WordPress, drop `index.html` into a `/journal/` directory on your server. The QR codes in the printed journal point to `stellarliving.com/journal#w[N]`.

## URL Structure

Each week has an anchor ID:
- `yoursite.com/journal#w0` → Week 0: The Year Ahead
- `yoursite.com/journal#w2` → Week 2: Serve First — The Vision
- `yoursite.com/journal#w11` → Week 11: World Down Syndrome Day
- `yoursite.com/journal#w51` → Week 51: Year in Review
- `yoursite.com/journal#share` → Share Your Story section

The page auto-scrolls to the correct week when opened from a QR code.

## Adding Content

To add a video or article link to a week, find the week's card in `index.html` and add a link inside the `wk-links` div:

```html
<div class="wk-links">
  <a class="link-video" href="https://youtube.com/watch?v=..." target="_blank">▶ Watch: Topic name</a>
  <a class="link-article" href="https://stellarliving.com/blog/..." target="_blank">📄 Article title</a>
</div>
```

Available link styles:
- `link-video` — blue (for YouTube/video content)
- `link-article` — green (for blog posts/articles)
- `link-foundation` — pink (for Foundation/donation links)

## Files

```
├── index.html          # The landing page (single file, no build needed)
├── 404.html            # Redirect fallback for GitHub Pages
├── _config.yml         # GitHub Pages config
├── CNAME_EXAMPLE       # Rename to CNAME if using custom domain
├── README.md           # This file
└── .gitignore
```

## QR Codes in the Journal

The printed journal contains 52 "Go Deeper" QR codes, one per week. Each QR encodes:
```
https://stellarliving.com/journal#w[WEEK_NUMBER]
```

If you deploy to a different URL, you'll need to regenerate the QR codes in the journal PDF to match.

## License

© 2027 Stellar Senior Living. Internal use.
