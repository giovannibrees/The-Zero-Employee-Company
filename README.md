# The Zero-Employee Company - Book Website

One-page marketing site for the book **The Zero-Employee Company** by Giovanni Brees, optimized for search and AI-assistant ranking.

Static site, zero build step: one HTML file, one author photo, one social share image. Deploys to Cloudflare Pages as-is.

## Files

| File | Purpose |
|---|---|
| `index.html` | The complete site (styles inlined, JSON-LD structured data for Book, Person, and FAQPage) |
| `assets/author.png` | Author photo |
| `assets/og-cover.jpg` | 1200x630 social share image |
| `404.html` | Not-found page (served automatically by Cloudflare Pages) |
| `robots.txt`, `sitemap.xml` | Search engine indexing |
| `_headers` | Security and cache headers (read natively by Cloudflare Pages) |

## Deploy to Cloudflare Pages (Git integration)

1. [dash.cloudflare.com](https://dash.cloudflare.com) -> Workers & Pages -> Create -> Pages -> Connect to Git.
2. Authorize GitHub and pick this repository.
3. Framework preset: **None**. Build command: (empty). Build output directory: `/`.
4. Deploy. Every push to the production branch redeploys automatically.

## Custom domain

The canonical URL is `https://thezeroemployeecompany.com`. Add the domain in the Pages project (Custom domains tab); Cloudflare handles DNS and SSL automatically if the domain is on Cloudflare.

## After deploy

- Validate structured data with Google's Rich Results Test (Book + Person + FAQPage).
- Submit the sitemap in Google Search Console and Bing Webmaster Tools (Bing feeds many AI assistants).
- Check the social card with a preview tool such as opengraph.xyz.

## Copy rules (binding)

- Never use em-dashes. Use "-".
- Never mention the author's location.
- Never say the author "sold" his operation - say "exited".
