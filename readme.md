# SEO / GEO / AEO / AIO / LLMO Package for balajirajaram.wikiseo.in

## Files in this package

| File | Purpose | Where it goes |
|---|---|---|
| `robots.txt` | Allows search engines **and** AI crawlers (GPTBot, ClaudeBot, PerplexityBot, Google-Extended, etc.) to read and cite the site | `https://balajirajaram.wikiseo.in/robots.txt` (site root) |
| `llms.txt` | Emerging standard (llmstxt.org) that gives LLMs a clean, structured summary of the site — improves how ChatGPT/Claude/Gemini/Perplexity describe you | `https://balajirajaram.wikiseo.in/llms.txt` (site root) |
| `llms-full.txt` | Fuller plain-text version of the whole profile for deeper LLM ingestion | `https://balajirajaram.wikiseo.in/llms-full.txt` (site root) |
| `sitemap.xml` | Standard XML sitemap for Google/Bing | `https://balajirajaram.wikiseo.in/sitemap.xml` (site root) |
| `meta-tags.html` | Improved `<head>` tags: title, meta description, canonical, Open Graph, Twitter Card, geo tags | Merge into your existing `<head>` |
| `schema-jsonld.html` | JSON-LD structured data: Person, ProfilePage, WebSite, FAQPage | Paste into `<head>` or before `</body>` |
| `faq-section.html` | Visible FAQ content (must match the FAQPage schema text) | Add as a new `<section id="faq">` before Contact, and add "FAQ" to your nav |

## Why each layer matters

- **SEO** (`meta-tags.html`, `sitemap.xml`, `robots.txt`): gets you indexed and ranked correctly by Google/Bing.
- **AEO** (`faq-section.html` + FAQPage schema): direct question-answer pairs are what answer engines (Google featured snippets, voice assistants) pull from.
- **GEO** (`schema-jsonld.html` Person schema + `llms.txt`): gives generative engines (ChatGPT, Perplexity, Gemini) unambiguous, structured facts to cite instead of guessing.
- **AIO/LLMO** (`llms.txt`, `llms-full.txt`, `robots.txt` AI bot allowances): makes the site easy for LLMs to crawl, parse, and quote accurately when someone asks "who is Balaji Rajaram."

## Implementation checklist

1. Upload `robots.txt`, `sitemap.xml`, `llms.txt`, `llms-full.txt` to the site root (same level as `index.html`).
2. Merge `meta-tags.html` into your current `<head>` — replace the existing title/description/OG tags.
3. Paste all four `<script type="application/ld+json">` blocks from `schema-jsonld.html` into `<head>`.
4. Insert the `faq-section.html` markup as a new section before "Contact," and add an "FAQ" link to your nav menu (`#home`, `#about`, `#expertise`, `#experience`, `#achievements`, **`#faq`**, `#contact`).
5. Add a real profile photo and set its URL in the `image` field of the Person schema and `og:image`/`twitter:image` — currently placeholders (`/assets/...`), update to your actual hosted image path.
6. Submit `sitemap.xml` in Google Search Console and Bing Webmaster Tools.
7. Validate structured data: https://validator.schema.org/ and https://search.google.com/test/rich-results
8. Re-crawl check in 1–2 weeks via Search Console URL Inspection.

## Notes

- Keep the FAQ text in `faq-section.html` and the FAQPage schema in `schema-jsonld.html` **identical** — mismatches hurt trust signals.
- Update `dateModified` in the ProfilePage schema and `lastmod` in `sitemap.xml` whenever you edit the page.
- If you add more pages later (e.g., a blog), extend `sitemap.xml` and `llms.txt` accordingly.
