# RESUME — read this first after /clear (state as of 2026-07-12)

## What this business is
**Webblaze** (renaming FROM "Curb" — rebrand not yet executed, waiting on domain confirmation).
We sell **$300 flat websites** to small businesses via cold outreach, then upsell lead-gen/marketing
retainers after they're paying customers. Goal: sell 10 websites at $300. Dad handles money/accounts
(Zayden is a minor — contracts & payments in dad's name).

## READ THESE FILES IN ORDER
1. `~/.claude/projects/-Users-zaydenzukerman-north-star-game/memory/bookedsolid_business_model.md`
   — full business model, all decisions, rebrand history, current state. THE master doc.
2. `ops/SETUP.md` — Zayden's setup checklist (domain, FreshBooks, address, FB account)
3. `outreach/cold-email.md` + `ops/FACEBOOK-OUTREACH.md` — the outreach scripts/playbooks
4. `outreach/leads-nowebsite.md` — verified/dead lead statuses (mostly burned; only Dune Buggy usable)
5. `ops/CLIENT-RESULTS-PLAYBOOK.md`, `ops/SEO-MARKETING-MASTER.md` — fulfillment + marketing research
6. `ops/REPO-LEVERAGE.md` — the /ads audit skill + camoufox we adopted from the IG post
7. `clients/dunebuggy/` — the finished 5-page spec site (live at zaydenzukerman-lang.github.io/curb/dunebuggy/)

## DECISIONS LOCKED (don't re-litigate)
- Payments: **FreshBooks** (dad's account, includes card processing). Not PayPal, not Stripe.
- Channel: **Facebook Messenger** + email. Targeting: business must have **ZERO website** (any other
  online presence OK). NEW dad principle: prefer businesses that NEED a site to make money →
  **high-ticket BOOKING niches**: fishing charters, wedding vendors (DJ/photog/planner), party/event
  rentals (bounce house/photo booth), contractors. NOT product e-commerce (Shopify's turf).
- Website = build FIRST, they pay only if happy. First Messenger msg has NO link (ask "want the link?").
- No AI mentioned publicly ever. Never fake personal claims (no "I tried your burger").
- **BUDGET RULE (violated twice, do not violate again): NO parallel research subagents. Do lead
  research directly in main thread via WebSearch/WebFetch. See feedback_token_budget.md.**

## VERIFICATION RULE (learned hard — cheap agents fabricated "no website" ~60% of the time)
Every lead: Claude probes domain patterns + checks directory/FB, THEN Zayden does final 10-sec check
on the business's FB page (Intro → Website field) before sending. Zayden is the last gate.

## IN-FLIGHT LEADS (just found, NOT yet verified — verify before any send)
High-payment-probability candidates from last search, all need domain-probe + FB-Intro check:
- Fishing charters, Orange Beach/Gulf Shores AL: Miss Brianna (fb/gulfshoresfishingcharter),
  Wild Orange Charters (fb/WildOrangeBeachFishing), Intimidator Sportfishing, Great Southern
  Fishing Charters, Orange Beach Fish Charter Services (since 1980)
- Charters Destin/PCB FL: Charter Boat Destination, Silver King Charters (Capt. Alex Hare)
- Party rentals: The Bounce House Co. (Schererville IN, fb/TheBounceHouseCo)
- Photo booth/wedding: Sittin Pretty Rentals (Collegedale TN, fb/sittinprettyrentals)
NOTE: charters especially tend to HAVE websites (many did in results) — verify hard, expect fallout.
NEXT ACTION was: probe these domains, then hand Zayden a verified send-sheet.

## STILL BLOCKED ON ZAYDEN (unchanged for days)
1. webblaze.io — bought? which registrar? (needed for rebrand + pro URL + email)
2. FreshBooks account (dad) — needed before first "yes"
3. Send the Dune Buggy Messenger message (msg 1 in cold-email.md / FACEBOOK-OUTREACH.md), do FB
   Intro check first. Their site is DONE. dunebuggyfoodtruck@gmail.com is their email.
4. Optional: install NotFair plugin (/plugin marketplace add nowork-studio/notfair ; /plugin install notfair@nowork-studio)

## TOOLS NOW AVAILABLE TO CLAUDE
- `/ads audit` skill installed (~/.claude/skills/ads) — paid-ads audit, basis for a "Webblaze Ad
  Audit" product ($150-300) for businesses already running ads.
- camoufox browser (~/.camoufox-venv) — anti-detect, for verification; Yelp still 403s headless.
- Repo: github.com/zaydenzukerman-lang/curb (will rename to webblaze on rebrand). Pages from /docs.
