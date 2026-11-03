---
name: site-serp-refresh
description: >-
  Keep an already-live crash-game affiliate site (Chicken Road, Aviator, Ice
  Fishing, Tower Rush) or a first-person branded casino site from falling behind
  in search. For a named live site, run a fresh, dedicated SERP + Ahrefs analysis
  for the current week, per geo, compare our live pages against the sites now
  ranking for each focus keyword, and apply SURGICAL add/replace/remove edits to
  the existing site (never a wipe-and-rebuild): new H2 sections for newly ranking
  intents, refreshed titles/meta/descriptions, replaced or added real images, and
  updated modified dates. Use when the user says "refresh", "update", "freshen",
  "re-optimise", "SERP check", "are we still ranking", or names a live site to
  bring back up to date.
---

# Site SERP Refresh

A maintenance skill for sites that are ALREADY BUILT AND LIVE. It does not build
new sites — the `crash-game-site` skill (github.com/bimal456/crash-game-site-skill)
does that. This skill keeps a live site current so it does not slip down the SERP
when competitors keep updating, when a game ships a new rule or a new sub-game,
when a new secondary keyword or a "<game> demo" intent starts ranking, or when the
published/modified date goes stale.

It applies to two site types, with the SAME content rules for both:

1. Crash / instant-win game sites — Chicken Road, Aviator, Ice Fishing, Tower
   Rush, and any future game. The site speaks directly to the player about the
   game in first person. The game is not ours; we still write in first person.
2. First-person branded casino sites — brands we run as our own, written in the
   brand's own first-person voice.

## Hard rule: surgical edits only, never a wipe

This is the most important rule in the skill. The site already exists and most of
it is fine. Change only what the analysis proves needs changing, and leave
everything else byte-for-byte untouched.

- Fetch the CURRENT live page first. Diff against what the new SERP says the page
  needs. Edit only the differing parts.
- One line needs to change -> replace that one line, not the paragraph around it.
- 10 images on a page and 4 are outdated/wrong -> replace those 4, keep the other
  6 exactly as they are.
- A title or meta is weak -> rewrite that tag only.
- A new intent is now ranking -> insert ONE new H2 section in the right place;
  do not touch the sections above and below it.
- Never regenerate a whole page or a whole site to make a small change. If a
  change cannot be made surgically, stop and report it instead of rewriting.
- Preserve existing structure, classes, IDs, the designed HTML/CSS hover blocks,
  internal links, cloaking paths and CTAs unless they are the thing being fixed.

## Hard rule: every geo is its own SERP, no translation

Each geo edition has its own Google result set. Do NOT translate the English page
into the other languages and call it done. For every geo, run a dedicated SERP
analysis in that geo's country + language and optimise that geo's title, meta
title, meta description, body content and images to ITS OWN SERP. Only reuse
content across two geos when their SERPs are genuinely the same (same ranking
sites, same intents, same angles). Otherwise each geo is optimised independently.

## Hard rule: voice and content (both site types)

Always first person. Write as "I / we / us / our" talking to the reader. Never
second or third person about the property itself: no "the game", "the brand",
"this website", "this homepage", "this site", "this page". Fix any such phrasing
found on the live site while refreshing.

Never present the site as a review, an information site, a guide, or an
independent/unofficial third party. Banned on every page, in every language,
including reworded dodges of these:

- "review", "verdict", "editorial team", "we tested", "independent",
  "information" / "informational" (including "information only, not advice"),
  "guide" and localised equivalents (e.g. Dutch "ontdek" is also banned in meta).
- "Contains promotional links." and every localised equivalent — not in the
  opening block, not in the footer. (rel="nofollow sponsored noopener" on CTAs is
  the only disclosure.)
- "we are not <operator> / not the casino / not the operator / no games hosted
  here / we fill a gap left by scams / no payment changes what we publish / we can
  be wrong / we are a small team" — any independent-site origin story or
  editorial-integrity framing.
- Never mention "KAP Digital" or "KAP" anywhere.

Keep everything that is a standing project rule:

- Titles: focus keyword first, commercial modifiers, current year, max 60 chars,
  carrying the geo's ACTUAL focus keyword (e.g. "aviator game", not the generic
  "crash game"), not a blog/info-article title.
- Meta descriptions: focus keyword at the start, 158 characters, include the
  current year, no listicle words, vary the wording each time (no reused
  feature-list template), and never the words learn / discover / explained /
  ontdek.
- No "#" fragment links anywhere. No 18+ badge or filter. No pop-up, modal,
  overlay or interstitial of any kind. No visible promotional-disclosure line.
- Affiliate cloaking stays: CTAs point to the on-site path (single-brand -> /login,
  broad/multi-brand -> /play), that path redirects to the real tracking link, is
  Disallow-ed in robots.txt and noindex+nofollow, and the real tracking URL never
  appears in crawlable HTML. Every CTA shows the full <domain>/play on hover
  (absolute URL), rel="nofollow sponsored noopener", target="_blank".
- Designed sections stay as hover-effect HTML/CSS (not flat). On WordPress sites,
  keep body/headings/FAQ as native Gutenberg blocks and each designed section as
  its own per-section Custom HTML block.
- Keep the global requirements intact: http->https, consistent internal link
  formatting, working 404/403, hreflang across geos, EEAT signals, canonical.

## Structure, headings, links and technical (every run, per geo)

- Headings and tags: SEO-optimise the H1, every H2 and H3 subheading, the title
  and the meta title to the latest SERP for that geo's focus keyword. They should
  carry the focus keyword and its current secondary keywords/intents naturally, in
  the framing the ranking pages use this week. Rewrite only the headings/tags that
  are off the current SERP; keep the ones that still hold.
- Internal linking: link meaningfully, never bombed in. Every internal link must
  fit its anchor context and point to a genuinely related, geo-correct page. No
  stuffing, no repeated same-anchor links, no link added just to hit a count. Add a
  missing useful link, re-point or remove a forced/irrelevant one. Keep internal
  link formatting consistent (absolute, one variant) so ranking does not split, and
  no "#" fragment links.
- Schema (JSON-LD): keep and fix structured data on every page — correct type for
  the page, datePublished/dateModified updated on changed pages, FAQPage on the FAQ
  and BreadcrumbList where used. Add schema the ranking pages use where it genuinely
  fits. Never add review/rating schema — we are not a review site.
- hreflang: a complete, correct cluster across every geo edition — each geo
  references all the other geos plus x-default, reciprocal and self-referencing, with
  the right locale code per geo (e.g. en-CA for the Canada edition). Fix any missing,
  one-way or wrong-locale tags. Canonical is self-referential per geo.
- Page set and header nav: the five mandatory pages must exist on every geo — About
  us, Contact us, Responsible Gambling, Terms & Conditions, Privacy Policy. About us,
  Contact us, Responsible Gambling and Privacy Policy must be reachable from the
  HEADER navigation on every geo; if any is missing from the header, add it. The
  other pages must match that game/geo's SERP: if a top-ranking site has a relevant
  page we do not have (a demo page, a bonuses page, a how-to-play/strategy page,
  etc.), build it, SEO-optimise it to that geo's SERP, link it meaningfully and add
  it to the nav and sitemap. Never carry a page list over from a previous build.
- robots.txt and sitemap: verify robots.txt allows the site and keeps the cloaking
  path Disallow-ed; verify the XML sitemap exists, lists every live page across all
  geos, drops removed URLs, adds new pages, and is referenced in robots.txt. Fix
  surgically.
- Image alt text: every image (kept, replaced or new) carries correct, descriptive
  alt text with the geo's focus keyword used naturally — never empty, duplicated or
  keyword-stuffed.

## Before starting (read these every run)

1. The target site's own memory file / area note (hosting, deploy method,
   editions/geos and languages, affiliate link + cloaking path, page set, focus
   keyword per page/geo, and any site-specific decisions). The deploy method is
   recorded there — use it, do not assume.
2. The project preferences (cloaking, voice bans, title/meta rules, page-set
   rule, image-prompt rule).
3. The `crash-game-site` build skill repo, for the standing build conventions the
   site was made with.

Confirm with the user: the site/domain to refresh, and (if they have not said)
that scope is the whole site — homepage + every other page, across every geo.

## The refresh workflow

Run this per geo edition, and within a geo, per page (homepage first, then each
other page) against that page's focus keyword.

### 1. Snapshot our live page

Fetch the current live URL for this geo/page. Capture its title, meta title, meta
description, H1, H2/H3 outline, body sections, images (count + what each shows),
internal links, published date and modified date, and any leftover banned voice.

### 2. Dedicated SERP analysis for this geo + focus keyword

Pull the live top 10 for the focus keyword in THIS geo's Google (correct country
and language). For the top-ranking sites record:

- Title, meta title, meta description.
- Full heading outline (H2s, then Conclusion, then FAQ, then the H3 FAQ
  questions — plain-list order).
- Content style split as percentages (points/tables vs paragraph), then CAP the
  points+tables figure at 30% max (paragraph 70%+) for what we write.
- Recommended word count based on the competitors' word counts.
- Images / visuals they use and how fresh they look.
- Their published/updated dates.
- New sections/intents that appeared since our last build: a new sub-game, new
  game rules, a "<game> demo" section, a new bonus/feature, a new focus keyword.

### 3. Ahrefs check for this geo

- Our site's current organic keywords and positions for this page (and GSC data
  if connected) — what we rank for, where we slipped, what we lost.
- Newly ranking secondary keywords the competitors gained this week, keyword
  gaps, and any intent that is rising that we do not cover.
- One intent = one keyword: fold word-order flips and synonym variants into a
  single keyword. One primary keyword per page/geo; list the rest as secondaries.

### 4. Gap analysis (this geo/page)

Decide, specifically, what is out of date versus the current SERP:

- Title / meta title / meta description: still competitive? Carries the geo's
  focus keyword + commercial modifier + current year? Within length limits? Any
  banned word? -> rewrite the tag(s) that fail, nothing else.
- Content coverage: which ranking subtopics/sections are we missing (new
  sub-game, demo, new rules, new feature)? -> each missing intent becomes ONE new
  H2 section of best-in-class content (not review/info voice, first person),
  with a real image placed in it.
- Thin or stale sections we already have: tighten only the specific lines that
  are weak; do not rewrite good paragraphs.
- Images: which specific images are outdated/wrong/missing versus what the SERP
  now shows? -> replace only those; add a real image for any new section.
- Freshness: is our modified date stale while competitors updated recently? ->
  update it (see step 6).
- Leftovers from the original build: any "review / information / guide / this
  website / this homepage / contains promotional links / independent" wording, or
  second/third-person voice -> fix to first person, surgically.

### 5. Apply surgical edits

Make the minimal set of edits from step 4 directly in the live page's markup:

- Replace only the failing title/meta/description tags.
- Insert each new H2 section at the correct position, leaving neighbours
  untouched. Best content for the intent, first person, matching the site's
  existing design (reuse an existing hover-effect block style, varied across the
  page; never collapse the page to one style).
- Replace only the specific images identified. For every image placed or
  replaced, put a REAL, relevant image in position so the page is not left behind;
  additionally output a copy-paste-ready image brief (one self-contained prompt per
  image, per the project image-prompt rule) for the designer to swap in a bespoke
  version later if wanted. Set descriptive alt text carrying the focus keyword
  naturally.
- Keep cloaking, CTAs, internal links, hreflang, canonical and designed blocks
  intact unless they were flagged.
- Do the same per geo with that geo's own SERP output — not a translation of the
  English edits.

### 6. Dates

On every page actually touched, update the modified/updated date to today so the
freshness signal fires (and the published date to today where that site's
workflow calls for it), in both visible byline and schema (datePublished /
dateModified). Do not bump dates on pages you did not change.

### 7. Deploy

Deploy using the method recorded in that site's memory file — do not assume:

- Cloudflare Pages sites: apply via Claude in Chrome on the Cloudflare dashboard
  (upload the changed files, click Save and deploy).
- cPanel static sites: per that site's zip/replace convention.
- WordPress sites: via the wp-admin browser-console method (window.name transfer +
  wp.blocks.createBlock/serialize), keeping prose/headings/FAQ as native Gutenberg
  and designed sections as per-section Custom HTML blocks.

Apply and deploy automatically, then report.

### 8. Report (per geo)

For each geo/page, output a change log:

- Focus keyword + the geo's current top sites.
- Gaps found (keywords, sections, images, tags, freshness, leftover voice).
- Exactly what was added / replaced / removed (diff-style), and what was left
  untouched.
- New keywords now targeted and new H2 sections added.
- Images replaced/added (+ the image briefs).
- Dates updated. Deploy status.

## Run checklist

- [ ] Read the site's memory file, project preferences, and the build skill repo.
- [ ] Confirmed domain + whole-site scope with the user.
- [ ] For EACH geo and EACH page: snapshot live -> dedicated SERP -> Ahrefs ->
      gap analysis -> surgical edits -> dates -> deploy -> report.
- [ ] No page wiped or regenerated; untouched content left byte-for-byte.
- [ ] No translation reuse unless two geos share the same SERP.
- [ ] First person everywhere; zero banned voice; titles/meta per the rules.
- [ ] H1/H2/H3 subheadings + title + meta title optimised to this week's SERP.
- [ ] Internal links meaningful and geo-correct, not bombed in; one URL variant.
- [ ] JSON-LD schema correct and dated; FAQPage/BreadcrumbList where fitting; no
      review/rating schema.
- [ ] hreflang cluster complete and reciprocal across all geos + x-default;
      canonical self-referential.
- [ ] Five mandatory pages present; About/Contact/Responsible Gambling/Privacy in
      the header; any SERP-relevant new page built and optimised.
- [ ] robots.txt correct (cloaking path Disallow-ed); sitemap complete and linked.
- [ ] Cloaking, CTAs, 404/403, http->https, EEAT intact.
- [ ] Real images placed; image briefs output; alt text correct on every image.
- [ ] Modified (and published where required) dates updated only on changed pages.
