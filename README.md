# spine-services

Website for Spine Services: https://spineservices.org

## How it runs

- **Host:** GitHub Pages, from the root of `main`. Every push to `main` goes live, usually within a minute.
- **In front:** Cloudflare (DNS, proxy, SSL mode Full, Web Analytics). `www` redirects to the non-www address.
- **Domain registrar:** Spaceship.
- **Email:** Zoho Mail. **Booking:** Calendly widget.
- **Stack:** plain HTML, CSS and JS in `index.html`, with no build step.

## Making changes

- HTML updates appear without a Cloudflare purge. Purge the cache only when replacing an image under the same file name (images are cached for up to 4 hours).
- The address in every canonical tag, social tag, sitemap and schema entry is `https://spineservices.org`, without `www`.
- Keep images small: WebP at about twice their display size. `og-image.jpg` stays JPEG at 1200x630 for link previews.
- `_headers` applies only to the leftover Cloudflare Pages copy (`spine-services.pages.dev`), which is set to noindex.
