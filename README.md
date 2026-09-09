# NDA Batch 2026-27 — Landing Page

Static landing page for **The Winning Edge Defence Plus**, Dehradun — the NDA 2026-27
classroom batch at the new Shiv Shakti Tower (Donali Chowk) centre.

## Campaign facts baked into the page

| | |
|---|---|
| Classes start | 18 September 2026 |
| Free demo classes | 18 – 30 September 2026 |
| Timing | 4:00 – 7:00 PM, Monday to Friday |
| Weekly test | Every Saturday |
| Batch valid till | April 2027 |
| Fee | ₹20,750 (regular ₹45,500) |
| Centre | Shiv Shakti Tower, Near Donali Chowk, Dehradun |
| Call | +91 8437001122 |
| WhatsApp | +91 7417920356 |

## Structure

```
index.html                          markup + SEO/schema head
assets/css/style.css                all styles
assets/img/logo.png                 brand logo (header, footer, favicon, OG)
assets/img/col-amardeep-singh.png   hero portrait
vercel.json                         caching + security headers
robots.txt / sitemap.xml
```

No build step, no dependencies, no JavaScript — it is plain HTML and CSS.
The illustrations in the "What clearing the NDA actually takes" section are
inline SVG, so they stay sharp at any size and cost no extra requests.

## Local preview

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
```

## Deploying

Pushes to `main` deploy automatically via Vercel.

## Editing the campaign copy

Dates, timings and the fee appear in more than one place. When the batch
changes, update all of these:

1. `<title>` and the `description` meta in `index.html`
2. The `og:` / `twitter:` description tags
3. The JSON-LD block (`startDate`, `endDate`, `offers.price`)
4. Hero kicker, `<h1>`, the demo-class note
5. The facts strip (5 cells)
6. The fee card
7. The schedule timeline (4 rows)

## Live URL

https://anubhav-d-rana.github.io/weda-nda-2026-27/

If the site later moves to Vercel or a custom domain, update the absolute URLs
in `index.html` (canonical, `og:url`, `og:image`, `twitter:image`, and the
JSON-LD block), plus `robots.txt` and `sitemap.xml`.
