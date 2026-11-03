# site-serp-refresh

A Claude skill that keeps an already-live affiliate site from slipping down the
SERP. It is the maintenance companion to
[crash-game-site-skill](https://github.com/bimal456/crash-game-site-skill) (which
builds new sites). This one refreshes sites that are already built and live.

Works for crash / instant-win game sites (Chicken Road, Aviator, Ice Fishing,
Tower Rush) and for first-person branded casino sites.

## What it does

Point it at a live site. For the whole site (homepage + every page), and for
every geo edition separately, it:

1. Snapshots the current live page.
2. Runs a fresh, dedicated SERP analysis for that geo + focus keyword (no
   translating the English page — each geo gets its own analysis).
3. Checks Ahrefs for new secondary keywords, ranking drops and gaps.
4. Compares our page against the sites now ranking: title, meta title, meta
   description, headings, content coverage, images, freshness.
5. Applies **surgical** add / replace / remove edits only — never a wipe. New
   intents become new H2 sections with real images; weak tags get rewritten;
   outdated images get swapped; modified dates get bumped.
6. Deploys using that site's recorded deploy method and reports every change.

## Why

SEO moves every week. A page that ranks today can drop when a competitor keeps
updating, when a game ships a new rule or sub-game, when a "<game> demo" intent
starts ranking, or when the modified date goes stale. This skill catches that and
brings the live site back up to date without disturbing what already works.

## Use

In a Claude session where this skill is available, name the site and ask to
refresh it, for example: "refresh chickenroad.radio.am" or "SERP check aviator
site, are we still ranking". Read `SKILL.md` for the full workflow and rules.
