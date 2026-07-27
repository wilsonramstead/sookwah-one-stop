# Sookwah One Stop Shop LLC — demo site

Single-page demo for **Sookwah One Stop Shop LLC**, an auto repair **and** body-work shop in
Winter Haven, FL. Built demo-first (noindex) to pitch. Not deployed / not committed by the build
step.

## Business

- **Name:** Sookwah One Stop Shop LLC
- **Trade:** Auto repair + body work (mechanical AND collision/body under one roof)
- **Address:** 1885 Executive Rd Ste 1875, Winter Haven, FL 33884
- **Phone:** (863) 331-5994 → `tel:+18633315994` / `sms:+18633315994`
- **Rating:** ⭐ **5.0 / 165 reviews** — perfect record, headlined throughout
- **Web presence:** none (no existing website)

## The angle

"One stop means one stop." The differentiator is that mechanical repair and body work happen in
the **same shop, same visit** — a customer can get a fender straightened and an A/C condenser
replaced in one drop-off instead of bouncing between two shops. Supporting themes pulled straight
from the reviews: honesty about what you do/don't need, expectations set from the first call,
communicating every step, staying late to finish, working to save the customer money, and
short-notice fit-ins. Ryan is named once (staying late); everything else is company/team framing —
no owner shrine.

## Reviews used (3 cards, real names, verbatim themes)

- **April Courrege** — brakes; honest about what she needed and didn't, communicated every step,
  stayed late, tried to save her money.
- **Isak Car** — fender fixed + A/C condenser replaced in one visit; "solid work without the
  runaround."
- **Ariana Lora** — short-notice fit-in; honesty and transparency "rare to find."

## Services shown

Brakes · A/C & Cooling · Body Work · General Repair · One-Stop Combos (two fixes, one drop-off) ·
Maintenance. All generic-safe; nothing invented.

## Design

- **Display font:** Marvel (700) — headings, labels, numerals
- **Body font:** Atma (400/500/600/700) — warm, rounded, approachable
- **Palette (unique across the portfolio):**
  - Espresso base `--ink #1B140F`, panels `--coffee #241A13` / `#2F2318`
  - Warm bone sections `--bone #F7F0E3` / `--bone-2 #EFE4D0`, card `#FBF6EC`
  - Primary accent (vermilion/persimmon) `--flame #E85B2B` (hi `#FF7B47`, lo `#C3461B`)
  - Gold for the 5.0 rating `--gold #EDAE39` / `#FFC85E`
  - "Garage espresso + vermilion + gold" — no other site in the portfolio uses this base or the
    Marvel/Atma pairing.

## Images (Unsplash — all HTTP 200, viewed for fit, globally unique across `websites/*`)

| Slot | Photo ID |
|------|----------|
| Hero — organized repair bay + tool chest | `photo-1729792706191-08f3ed158650` |
| One-roof / mechanical — open engine bay | `photo-1716385136931-39096a54870f` |
| One-roof / body — spray-painting a panel | `photo-1666009387246-65e8ad8e7103` |
| Service — Brakes (yellow caliper + rotor) | `photo-1759189901164-900e0afac895` |
| Service — A/C (dash & climate controls) | `photo-1715597964018-b9ecfd21574e` |
| Service — Body work (car masked in booth) | `photo-1512080482556-ea648017576c` |
| Service — General repair (under the car) | `photo-1783427404359-31e2264ec9ed` |
| Work gallery — dent/panel inspection | `photo-1729554981212-6557ef8e4835` |
| Work gallery — team working after hours | `photo-1577801347781-d9d9362657b7` |

Base URL pattern: `https://images.unsplash.com/<photo-id>?auto=format&fit=crop&w=...&q=80`.
"A look at the work" tiles are labeled **Sample** and pitched as placeholders to be swapped for
real shop photos after sale.

## Verification (AUTOMATION.md checklist — all pass)

- `noindex` meta + `<!-- DEMO: remove noindex -->` comment present
- E.164 links only: `tel:+18633315994` / `sms:+18633315994` (no malformed variants)
- `og:image` absolute; `og:url` = `https://wilsonramstead.github.io/sookwah-one-stop/`;
  `twitter:card = summary_large_image`
- Footer credit "Website by Wilson Innovations" → https://wilsoninnovations.net
- JSON-LD `AutoRepair` with `aggregateRating` 5.0 / 165
- No fixed call bar (`position:fixed` absent); sticky header call button visible at 390px
- No owner-shrine section; Ryan named once
- Invented nothing: no email, hours, license/insured, 24-7, founding year, certifications
- Mobile guardrails: `html,body{overflow-x:clip}`, brand name wraps ≤560px, longhand vertical
  padding on padded containers, `min-width:0` on grid/flex children (17 uses),
  `overflow-wrap:break-word`
- All 9 Unsplash IDs HTTP 200 + 0 collisions across `websites/*/index.html`
- Fonts Marvel + Atma unused by any other site; signature hexes unique

## Domain

- **sookwahonestop.com — AVAILABLE** (RDAP 404), ~$11/yr (Porkbun/Cloudflare).
- Business has no existing domain to point. Recommend registering `sookwahonestop.com` at launch.

## Deploy notes (not done here)

`og:url` already targets `https://wilsonramstead.github.io/sookwah-one-stop/`. When Wilson is
ready: git init + commit in this folder → `gh repo create wilsonramstead/sookwah-one-stop
--public --source . --push` → enable Pages (master, `/`). Remove `noindex`, swap in real photos,
point the domain after payment.
