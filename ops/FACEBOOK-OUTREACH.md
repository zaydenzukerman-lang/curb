# Webblaze — Facebook Messenger Outreach Guide (for someone who's never used Facebook)

Targeting rule (Zayden, 2026-07-10): leads can have ANY online presence (Facebook, Instagram,
Google listing, Yelp) — they just can't have a **website**. Zero website = valid target.

## Part 1 — Set up your account (15 min, once)

1. Go to facebook.com → **Create new account**. Real name (or "Z [Lastname]"), an email you check,
   your birthday. It will text/email a verification code — enter it.
2. **Make the profile look human before messaging anyone** (this matters — accounts with no photo
   and no activity get flagged as spam bots):
   - Add a profile photo (a real one of you, or a clean Webblaze logo — real photo works better)
   - Add a cover photo (anything non-empty)
   - Bio line: "I build websites for small businesses."
   - Add a few friends if you can (family counts), like a handful of pages, scroll the feed a bit
3. **Warm it up for 2-3 days before any outreach.** Log in daily, browse, like a few things.
   Facebook watches brand-new accounts hard — a day-one account that instantly messages 10
   businesses looks exactly like a bot and gets restricted.

## Part 2 — How to find and message a business (the actual mechanics)

1. **Search bar** (top of the page, magnifying glass on mobile) → type the business name from the
   lead list → tap the result with the little "Page" label or their logo.
2. On their page you'll see a blue **"Message"** button (sometimes under the ⋯ menu). Tap it —
   that opens Messenger, which is just Facebook's texting app.
3. Type/paste the script (below), personalize the [brackets], send. Done. That's the entire skill.
4. Replies show up under the **Messenger icon** (chat bubble, top right). Check it during your
   4-hour window; reply within 2 hours max.

Notes:
- You're messaging their business Page, not a person's private profile. Pages EXIST to receive
  messages from strangers — this is normal, expected behavior, not creepy.
- Never message the same business twice in one day. One follow-up 3 days later max, then done.

## Part 3 — Volume rules (protect the account)

- Week 1: **max 5 new businesses/day.** After that: 10/day ceiling. Messenger bans for spam are
  fast and permanent — low volume, high personalization, always.
- **First message: NO LINKS.** New accounts sending links = instant spam filter. Make them reply
  first, then send the demo links in message #2. (This also boosts reply rates — same trick as
  the linkless email.)
- If Facebook ever shows a warning or asks you to verify — stop outreach for 48h, browse normally.

## Part 4 — The scripts

**Message 1 (opener — no links):**
> Hey! I came across [Business] here on Facebook — noticed you don't have a website, just the
> page. I build websites for small businesses ($300 flat, no monthly fees). I build yours first
> and you only pay if you're happy with it. Want me to send a couple examples of my work?

**When they reply "sure" → Message 2 (now links are invited):**
> Here you go: [demo link 1] and [demo link 2] — both built by me.
> Same idea for [Business]: I'll put yours together this week, you tell me what to change, and
> it's $300 once you like it. No contract, nothing monthly. Want me to start?

**Follow-up (3 days, only if no reply, only once):**
> Hey — just floating this back up. If a website's not something you want right now, all good,
> just say the word and I'll leave you be.

**Closing (they said yes to the built site):**
> Awesome. I'll email you an invoice for the $300 (pay by card right from the email) + a quick
> one-page agreement. The moment that clears, the site's live and it's yours.

All other replies ("why so cheap," "who are you," "can you do marketing too") — use the same
answers as outreach/cold-email.md's Reply Playbook. Same product, same rules, different app.

## Part 5 — Log everything
Same rule as email: every contact goes in the lead file — date, message #, status
(sent/replied/pitched/building/closed/dead). If they say "no," they go on the never-again list.


## Part 6 — Assisted sending (Claude drives YOUR Chrome) — starts AFTER warmup week
Decided 2026-07-10 (Zayden's call, guardrails below are the condition):
- After the account is ~1 week old with real human usage AND Zayden has sent the first messages
  manually, Claude takes over day-to-day sending — 3-6 messages/day max, each written fresh from
  that lead's actual page, randomized human-like spacing across the session.
- HOW: Zayden runs the `webblaze-chrome` launcher (Chrome with a debug port) on his machine; Claude
  drives that real, already-logged-in browser via DevTools. NEVER a fresh/automated browser
  profile, NEVER headless, NEVER from another machine.
- HARD TRIPWIRES: any captcha, "confirm your identity" checkpoint, warning banner, or unusual
  logout → automation stops for 72 hours minimum, Zayden browses manually, we reassess. Any
  restriction repeat = channel goes fully manual for good.
- Replies stay human-reviewed: Claude drafts, Zayden approves/sends replies during his window
  (speed matters more on replies than on openers).
