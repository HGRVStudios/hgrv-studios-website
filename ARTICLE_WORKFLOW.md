# HGRV Publications: article workflow

This is a static GitHub Pages site. There is no paid CMS or build step. The site has **zero published articles** in the starter package. Do not mark drafts as published before review.

## Publish an article
1. Copy `articles/_article-template.html` to `articles/your-article-slug.html` (lowercase words separated by hyphens).
2. Replace every `REPLACE` placeholder, and remove the `noindex,nofollow` meta tag **only after** final editorial review. Add a truthful SEO description and article date.
3. Confirm every claim and source. Disclose AI assistance and whether the content is research-only or personally tested. Don't fabricate author identities, first-hand experience, prices, ratings, stock, or testing.
4. If affiliate links are included, put a clear disclosure *before* them, follow affiliate network requirements, and use `rel="sponsored nofollow"` on commercial outbound links. Update the site-wide disclosure and privacy pages for any newly used services. Do not add affiliate links before program approval.
5. Add an object to `data/articles.json` with the exact page slug, category, title, summary, ISO date, reading time, and `"status":"published"`. Example:

```json
[
  {
    "slug": "example-guide",
    "category": "kitchen",
    "title": "Example guide title",
    "summary": "Short, original summary.",
    "date": "2026-11-12",
    "readTime": "6 min read",
    "status": "published"
  }
]
```

Allowed category keys: `home-living`, `technology`, `kitchen`, `workshop`, `outdoors`.

6. Upload both the article HTML file and changed `data/articles.json` to GitHub. The homepage, Articles page, and category pages will then show it automatically, newest first. Keep unpublished drafts out of `articles.json` or use `"status":"draft"`.
7. Test article links, navigation, mobile layout, spelling, disclosures, and external sources on the live domain. Verify indexing in Google Search Console when ready.

## Notes
- The homepage's featured section displays the latest 3 published articles.
- All category pages are prebuilt and show a clear empty state until articles are published.
- The `_article-template.html` is deliberately noindex and excluded from the article list. Do not share it as a live article.
- JavaScript fetches `data/articles.json`. Opening HTML files directly via `file://` may not load the index; test on GitHub Pages or a local HTTP server.
- This site does not yet include analytics, tracking, advertisements, or affiliate links. Review privacy/disclosure text before enabling them.
- Once a production domain is confirmed, add canonical URLs, sitemap.xml, Open Graph URLs, and Search Console verification. Avoid guessing the final publication URL.
