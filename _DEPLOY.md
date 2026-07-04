# Nationwide site — FOLDER delivery

This is ONE ordinary static website. Every internal link is relative, so it runs
on any static host with no special configuration.

## Upload to shared hosting (Hostinger, cPanel, Namecheap, GoDaddy…)
1. Unzip this folder.
2. Upload everything inside it into your hosting web root (usually `public_html`).
3. Point your domain at the host. Visit https://yourdomain.com — done.
   (`.htaccess` already wires the custom 404 + caching on Apache/LiteSpeed hosts.)

## Drag-and-drop hosts (Netlify, Cloudflare Pages, Vercel)
Drop this whole folder into the dashboard's deploy area. NOTE: Cloudflare Pages
caps at ~20,000 files — fine for a capped build, not an all-cities one.

## Custom domain + SEO
- If you entered your domain before generating, canonicals, sitemap.xml,
  robots.txt and JSON-LD schema already point to it — nothing to edit.
- If not, find-and-replace `{{SITE_BASE_URL}}` with `https://yourdomain.com`
  across the .html / .xml / .txt files before uploading.
- Submit `https://yourdomain.com/sitemap.xml` to Google Search Console.

## What's inside
- `index.html` — homepage / states directory
- `about.html`, `contact.html`, `services.html`
- `<state>/index.html` — state hub (lists every city)
- `<state>/<niche>-in-<city>.html` — city pages
- `sitemap.xml` (+ chunked children if large), `robots.txt`, `404.html`, `assets/`
