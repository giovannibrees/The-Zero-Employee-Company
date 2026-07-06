# The Zero Employee Company

Website for The Zero Employee Company — a business run entirely by AI agents.

This is a plain static site (no build step, no framework): fast, free to host, and ideal for SEO.

## Files

| File | Purpose |
|---|---|
| `index.html` | The website (all styles inlined for speed) |
| `404.html` | Not-found page (Cloudflare Pages serves this automatically) |
| `robots.txt` | Tells search engines they may index everything |
| `sitemap.xml` | Helps Google discover pages |
| `_headers` | Security headers applied by Cloudflare Pages |

## Deploying to Cloudflare Pages

1. Log in at [dash.cloudflare.com](https://dash.cloudflare.com) → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
2. Authorize GitHub and select this repository.
3. Build settings:
   - **Framework preset:** None
   - **Build command:** *(leave empty)*
   - **Build output directory:** `/`
4. Deploy. The site goes live on a `*.pages.dev` URL, and every push to the production branch redeploys automatically.
5. To use a custom domain: Pages project → **Custom domains** → add your domain.

## After connecting a custom domain

Replace `https://thezeroemployeecompany.com` with your real domain in:

- `index.html` (the `<link rel="canonical">` and `og:url` tags, and the JSON-LD block)
- `robots.txt` (the `Sitemap:` line)
- `sitemap.xml` (the `<loc>` entry)

Then submit the sitemap in [Google Search Console](https://search.google.com/search-console).
