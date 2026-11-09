# HGRV Publications: deployment and article workflow

## Before deployment
- Keep your backup of the current GitHub repository.
- This ZIP includes `CNAME` containing `hgrvstudios.com`. Do not delete it.
- No drafted articles or untested projects are publicly listed.
- No advertising or analytics scripts are installed.

## Upload to GitHub Pages
1. Open repository `hgrv-studios-website` on the `main` branch.
2. Use **Add file → Upload files** and drag the *contents* of this extracted folder, not the outer folder or ZIP.
3. GitHub's web uploader may not handle nested folder replacement reliably. If it does not preserve folder paths, use GitHub Desktop or Git command-line instead.
4. Commit changes and allow Pages to deploy. Check `https://hgrvstudios.com/`, `/articles.html`, `/free-projects.html`, `/sitemap.xml`.
5. Confirm `CNAME` remains in the repository root and Pages still shows the custom domain.

## Publish an article
- Copy `articles/_article-template.html` to `articles/your-slug.html`.
- Replace all `REPLACE` placeholders and remove the `noindex,nofollow` meta tag only when the article is ready.
- Add a `published` record to `data/articles.json` with slug, category, title, summary, date and readTime.
- Add the final article URL to `sitemap.xml`.
- Add canonical, Open Graph title/description/url and an `og:image` with a real, appropriately licensed absolute image URL once the featured image exists. Do not fabricate photos or testing.
- Check links and phone layout.

## Publish a free project
- Create and verify a full project page in `projects/slug.html`, then upload tested downloads under `downloads/`.
- Add a `published` record to `data/projects.json` with slug, category, categoryLabel, title, summary.
- Include materials, steps, dimensions, safety warnings, testing status, and an explicit license.
- Add its page URL to `sitemap.xml`.
- Do not add an ad click gate. Standard ad networks typically prohibit incentivized clicks; investigate eligible rewarded-ad formats separately before implementing.

## Sharing and Pinterest
- Pages include text-only Open Graph previews. When original featured images are available, add an `og:image` absolute URL, `twitter:card=summary_large_image`, and verify previews.
- Pinterest-ready graphics and a business account are separate tasks.

## Site operation
- No paid services or new dependencies.
- GitHub Pages is static. Project search filters the published `data/projects.json` index client-side.
