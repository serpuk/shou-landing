# Apartments offer page — campaign-readiness & domain decision (build#94)

**Question:** Is `shou.be/apartments/offer` good enough to launch a paid campaign, or should we register a separate domain? If so, what name?

**Short answer:** The *page* is strong and close to ready. Do **not** launch paid traffic to it yet — three things must land first (conversion tracking, one piece of social proof, an apartments-specific share image). A separate domain is **not needed** to launch; keep the campaign on `shou.be/apartments` and (optionally) register a short vanity domain that 301-redirects to it as a marketing asset — not a second site.

---

## The page itself — verdict: strong

A complete, professionally built conversion page: clear owner-focused value prop, benefit-led "six reasons," revenue framing, today-vs-shou comparison, live concierge showcase, multilingual "what guests ask" proof, owner dashboard/intelligence, how-it-works, scale (1→500), clear pricing (€19/apt/mo, first month free), risk-reversal, and a working self-serve CTA ("Start free" → dashboard signup). SEO basics present (title, description, OG tags, canonical, robots index). Fast (inline CSS, no blocking JS), responsive, theme-aware. A **live demo/sample** link is a big conversion asset.

## Blockers — fix before spending ad budget

1. **No conversion tracking anywhere on the site.** No GA4, Google Ads tag, GTM, or Meta pixel — the offer page has no `<script>` at all. Without a conversion event firing on "Start free"/signup you cannot measure cost-per-signup, optimize bids, build retargeting audiences, or know if the campaign works. **This is the #1 blocker** — running paid traffic without it wastes budget blind.
2. **No social proof.** The testimonial block is intentionally empty (no real customers yet). Cold paid traffic converts far worse with zero proof. Add at least one credible signal before scale: a real quote, a recognizable property/logo, an "N apartments already using shou," or an honest founder note.
3. **Generic share image.** `og:image` points at `og-this-week.png` (the events product), not apartments. Ad/social/link previews won't show an apartments-relevant creative. Needs a proper 1200×630 apartments image.

## Polish (not blocking)

- Sales page is **English-only** — the multilingual product is a selling point, but BE FR/NL paid traffic ideally gets localized copy or at least FR/NL ad → matched landing.
- **No lead-capture fallback** for visitors not ready to self-serve (email/newsletter) — "Start free → dashboard" is the only path.
- Campaign URL is long (`shou.be/apartments/offer`) — see domain note.

## Domain decision: subpath vs own domain

**Recommendation: launch on `shou.be/apartments`; do not spin up a separate site to launch.**

- Ad platforms don't care about subpath vs root. `shou.be/apartments/offer` inherits shou.be's domain age/trust, keeps one analytics setup, and avoids an SEO cold-start.
- **Optionally register one short vanity domain** (~€10-30/yr) and **301-redirect it to `shou.be/apartments`** — a memorable URL for ads, print flyers, word-of-mouth and sales emails, and brand protection. Redirect, don't clone (a duplicate site splits authority and creates duplicate-content problems).
- A true **standalone domain/site is only worth it later** if the apartments product is spun into its own brand distinct from "shou," or to rank organically for vertical queries independent of shou.be. Not needed for a first campaign.

*(Candidate vanity names were shared with the team in the working session and deliberately kept out of this public repo to avoid seeding squatters.)*

## Suggested follow-up tasks

- Add GA4 + Google Ads/Meta pixel with a signup conversion event (unblocks measurement).
- Add one real social-proof element to the offer page.
- Produce a 1200×630 apartments OG image and point `og:image` at it.
- (Optional) register + redirect a vanity domain; (later) FR/NL localized offer variant.
