# valekar.github.io: Valekar Studio

Site for an animated explainer-video studio. It's one static `index.html` with no build step and no frameworks.

- Brand, contact email and the contact-form endpoint are constants at the top of the last `<script>` in `index.html` (`BRAND`, `CONTACT_EMAIL`, `CONTACT_ENDPOINT`). The `<title>`/OG tags in `<head>` repeat the brand for crawlers.
- Motion is lightweight: a looping SVG "explainer" diagram in the hero (paused offscreen), CSS transform/opacity reveals via IntersectionObserver, click-to-load YouTube thumbnails, native scrolling, and `prefers-reduced-motion` support.
- Contact form posts JSON to `CONTACT_ENDPOINT` (a Cloudflare Worker relay to Telegram). If that's empty, it opens a prefilled email instead.

Live: https://valekar.github.io/
