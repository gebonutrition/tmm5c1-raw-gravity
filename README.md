# TMM5C1 — Raw Gravity × Take My Muffin

Production static landing adapted from the supplied `web.dc.html` and `mobile.dc(2).html` design references. The DC-only `support.js`, `<x-dc>` runtime, `<sc-if>` wrappers and mock submit handler are not used in production.

## Sections

- Desktop and mobile layouts switch at 767px, each preserving the corresponding supplied source layout.
- Infinite marquee, hero, energy-drink vs Raw Coffee comparison, mid-page CTA, testimonials, fan-price CTA, Klaviyo newsletter and footer.
- All Amazon buttons use the supplied Amazon Attribution URL.
- Meta Pixel `1632582321547641`: PageView on load; InitiateCheckout on Amazon CTA click; Lead + Contact after a successful newsletter submission.
- Newsletter uses `/api/subscribe.js` and Klaviyo.

## Vercel environment variables

Set these in the Vercel project settings, for Production, Preview and Development:

- `KLAVIYO_API_KEY`: full private Klaviyo API key; do not commit it to Git.
- `KLAVIYO_LIST_ID`: `RTNAsa`.

A local `.env.example` is provided, with no secrets.

## Deploy

Import the repository into Vercel as a static site with a Vercel Function under `/api/subscribe.js`. No build command or output directory is required. Attach `tmm5c1.rawgravity.coffee` after the first deployment.
