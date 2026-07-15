# Webblaze — Email Infrastructure Setup

## CURRENT NEED (2026-07-15): hello@webblaze.io for the marketing site's contact button
Decided: **free route**, not paid Workspace — this is low-volume inbound (people replying to the
webblaze.io site), not bulk cold-email sending, so full SPF/DKIM auth isn't needed yet.

**Dad's 5-minute checklist (needs his Namecheap login — Claude has no access to this account):**
1. Namecheap → Domain List → webblaze.io → Manage → **Email → Redirect Email** (free tier)
2. Add: `hello` → forwards to → [Zayden's real Gmail address]
3. Save — takes effect in a few minutes
4. In that Gmail: **Settings (gear) → See all settings → Accounts and Import → "Send mail as" →
   Add another email address** → enter `hello@webblaze.io` → follow the verification (Gmail
   emails a confirmation link/code to the forwarded address, which lands in this same inbox) →
   confirm
5. Done — you can now receive AND reply as hello@webblaze.io, 100% free, no dedicated inbox needed
6. Tell Claude once it's live → the mailto: contact button on webblaze.io stays exactly as-is,
   already points to hello@webblaze.io, nothing to change on the site side

**Upgrade path (later, only if cold-email volume grows):** the fuller Zoho/Google Workspace +
SPF/DKIM/DMARC setup below is still the right move once sending real *cold outreach* volume by
email (not just receiving replies) — revisit then, not now.

## Step 1 — Domain (10 min, with dad's card)
Buy **webblaze.io** at Cloudflare Registrar (at-cost, free DNS) or Namecheap. Dad's name/card.
STATUS: done — webblaze.io registered under dad's account 2026-07-10.

## Step 2 — Mailbox (10 min) — forwarding is NOT enough, we must SEND
(This is the upgrade path for cold-email SENDING at volume — not needed for the free hello@ setup above.)
Pick one:
- **Zoho Mail Free** — free, 1 custom-domain mailbox. Fine for us. zoho.com/mail → add domain → create hello@webblaze.io
- **Google Workspace** (~$7/mo) — nicer, Gmail interface. Either works.

## Step 3 — DNS records (10 min — paste these in the registrar's DNS panel)
Zoho/Google will show you the exact values during setup. You will paste:
1. **MX records** — mail delivery (from Zoho/Google setup screen)
2. **SPF** (TXT record) — e.g. Zoho: `v=spf1 include:zohomail.com ~all`
3. **DKIM** (TXT record) — generated in the Zoho/Google admin panel, copy-paste
4. **DMARC** (TXT record, name `_dmarc`): `v=DMARC1; p=none; rua=mailto:hello@webblaze.io`
Then send a test email to your personal Gmail → check it arrives NOT in spam → open
"show original" → confirm SPF: PASS, DKIM: PASS. Tell Claude the domain is live → I wire the
website contact button + quote form the same day.

## Step 4 — Mailing address (CAN-SPAM, required in every email footer)
Home address is legally sufficient and free — use it unless dad wants privacy, in which case a
P.O. box (~$12/mo) works too. 2-minute decision, not a purchase blocker.

## Step 5 — Warmup schedule (don't skip — new domains that blast get burned permanently)
- Days 1–2: email friends/family from the new address, get replies. 5-10 sends.
- Days 3–7: 10–15 cold sends/day max
- Week 2+: up to 25–30/day. Never more, never bulk tools, always personalized.
- Watch: if replies stop landing / you see bounces, STOP and tell Claude.

## Footer that goes on every cold email (compliance, already in templates)
> Webblaze · [P.O. Box ___, City, ST ZIP] · If you'd rather not hear from me, reply "no" and that's the end of it.
