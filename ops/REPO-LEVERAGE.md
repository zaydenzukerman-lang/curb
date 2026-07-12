# Repo Leverage — from the @bestapps.ai post (actioned 2026-07-12)

Source: instagram.com/p/Dap5_oIFRza — "6 GitHub repos that print money." The real message:
free tools → packaged as outcomes businesses pay for. Here's the triage and what was DONE.

## ✅ ADOPTED — directly serves Webblaze revenue

### 1. claude-ads (AgriciDaniel/claude-ads, ★6.9k, MIT) — INSTALLED
- **What:** Paid-ads audit skill for Claude Code. 250+ checks across Google/Meta/YouTube/LinkedIn/
  TikTok/Microsoft/Apple/Amazon Ads, weighted 0-100 Ads Health Score, prioritized action plan.
  A senior PPC auditor charges $1,500+ and takes 4-6 hrs; this runs in ~15 min.
- **Installed at:** `~/.claude/skills/ads` → available as `/ads audit`, `/ads google`, `/ads meta`, etc.
- **How it makes us money:**
  a) **New standalone product: "Webblaze Ad Audit"** — for businesses already running ads. We charge
     $150-300 (undercut the $1,500 market as newcomers), deliver a scored report + action plan.
     Great tripwire for bigger clients than the $300-website crowd.
  b) **Full Funnel fulfillment** — when we manage a client's Meta/LSA, monthly audits become part
     of the deliverable and the report.
  c) **Sales ammo** — "your current ads scored 61/100, here's what's leaking" is a devastating
     cold-outreach hook for businesses visibly running ads.
- **Note:** full audits need client ad-account access/exports (they grant read access or export
  data). Strategy-level reviews work from screenshots/manual data.

### 2. Camoufox (daijro/camoufox, ★10k) — INSTALLED (venv: ~/.camoufox-venv)
- **What:** anti-detect browser, drives like Playwright but fingerprints as a real user.
- **Why we need it:** our lead verification kept hitting 403s (Yelp, etc). Camoufox lets Claude
  actually read directory pages to verify "no website" claims before Zayden sends.
- **Usage boundary (hard rule):** lead RESEARCH/verification only. NEVER for Facebook/Messenger
  automation — the account-safety rules in FACEBOOK-OUTREACH.md stand unchanged.
- Browser binary fetched. Usage: `~/.camoufox-venv/bin/python`, `from camoufox.sync_api import Camoufox`,
  pages need `browser.new_page(no_viewport=True)` (protocol quirk with playwright 1.61).
- **Tested honestly (7/12):** loads pages fine, but Yelp STILL 403s in headless mode (PerimeterX-tier
  protection). Camoufox helps on softer directories; Yelp verification stays with Zayden's manual
  check / headful mode if ever truly needed. Not a silver bullet — logged so we don't re-learn this.

### 3. NotFair (nowork-studio/NotFair, ★3.1k) — NEEDS ZAYDEN (2 commands)
- **What:** Claude Code plugin: SEO audits, GEO (AI-search optimization), Google Ads + Meta Ads
  skills with direct account connections via MCP.
- **Install (Zayden runs in Claude Code):**
  1. `/plugin marketplace add nowork-studio/notfair`
  2. `/plugin install notfair@nowork-studio`
- **How it makes us money:** SEO audit skill supercharges our free-audit opener; Google/Meta MCP
  connections make Full Funnel fulfillment real (connect client accounts read-only, audit live).

## 🔖 SHELVED — real but not now

### 4. HyperFrames (heygen-com/hyperframes, ★34k) — "Write HTML. Render video."
- Could turn client sites into 15-sec promo videos (pitch ammo / a $75-150 add-on / social content
  for clients). Adopt when we have a paying client who'd buy it. Zero cost to wait.

### 5. Open-Generative-AI (★23k) — self-hosted image/video gen, 200+ models
- We already have image generation covered. Self-hosting models is heavy. Revisit if image costs
  ever matter.

## ❌ NOT OURS — flagged honestly

### 6. FinceptTerminal (★28k) + Vibe-Trading (★20k) — trading tools
- Not Webblaze. For Zayden's personal $500 options lane: these are DATA/RESEARCH tools, and better
  data ≠ edge — the same math from before stands. A Bloomberg clone doesn't change options odds.
  If he wants Fincept for learning/research, fine — it's free — but it is not a money printer.

## The meta-lesson (what the post actually teaches)
The repos aren't the product. **Packaging is.** "claude-ads" is free for anyone; the money is in:
audit → report → prioritized plan → retainer. That's already our exact model (site → audit →
lead-gen retainer) — these tools just deepen what we can deliver per tier.
