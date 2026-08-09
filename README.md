# Dominic Sherwood — static portfolio site

Slim, zero-maintenance replacement for the Shopify store. One HTML file, two hero images, no JavaScript, no build step, no dependencies. Hosted free on GitHub Pages.

## Editing

All content lives in `index.html` — text is plain HTML, styles are in the `<style>` block at the top. Edit, commit, push to `main`; GitHub Pages redeploys automatically in ~1 minute.

## Structure

- `index.html` — the whole site (hero, upcoming work, previous credits, about, contact)
- `images/hero-1200.jpg` / `hero-2000.jpg` — the licensed hero portrait (only licensed image; all other imagery was removed deliberately)
- `CNAME` — the custom domain GitHub Pages serves (`thedominicsherwood.com`)

## DNS (GoDaddy)

Point the domain at GitHub Pages:

| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | thecoachgreg.github.io |

Delete the old Shopify records (A @ → 23.227.38.65, CNAME www → shops.myshopify.com) first. Other domains (e.g. domsherwood.com): use GoDaddy domain forwarding (301) to https://thedominicsherwood.com.

After DNS propagates, enable **Enforce HTTPS** in the repo's Settings → Pages.

## Adding email capture later

Drop a Klaviyo (or MailerLite) embedded form into a new section in `index.html` — their embed snippets work on any static page. No other changes needed.
