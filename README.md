# partnerwithchiams

A one-page, bilingual (中文 / English) site inviting partners to support the Chiams' ministry.

- `index.html`: the page. Language: add `#en` or `#zh` to the link to open it in that language.
- `functions/api/give.js`: a Cloudflare Pages Function that opens a Stripe checkout for the donor's
  chosen currency (RM, SGD, AUD; minimum 10), amount, frequency and optional 4% fee cover.

## Cloudflare Pages settings
- Framework preset: None. Build command: (empty). Build output directory: `/`
- Variables and secrets (Production): `STRIPE_SECRET_KEY` (type Secret), a Stripe restricted key (rk_live_...).
  After adding or changing it, redeploy.
