# TapThrough — Canonical Brand & Product Reference

> The single source of truth for product identity, typography, color, voice,
> and pricing across **all** TapThrough surfaces — the iOS app, the marketing
> website, App Store Connect listing, App Store screenshots, social posts,
> press kit, and any future surface.
>
> **Rule:** if a value in this document conflicts with a value anywhere else,
> this document is correct and the other surface is stale. Update the stale
> surface in the same commit you find it.

_Last updated: 2026-05-15. Owner: Jeffrey Davis (Jedrock LLC)._

---

## 0. Quick reference (the 10 things you'll look up most)

| Field | Value |
|---|---|
| Product name | **TapThrough** (one word, capital T, capital T) |
| Operator | **Jedrock LLC** (California limited liability company) |
| Domain | `tapthrough.app` |
| Support email | `support@tapthrough.app` |
| Mailing address | 5751 Cabot Drive, Oakland, CA 94611, USA |
| Bundle ID | `org.jedrock.tapthrough` |
| App icon | A white glowing index-finger-tap silhouette against a deep violet gradient with a teal target dot. Master: `TapThrough/Assets.xcassets/AppIcon.appiconset/AppIcon-1024.png`. Web mirror: `tapthrough-site/img/icon.png`. |
| Brand dark gradient | `#0D0D1A → #1A1033 → #0F2044` (the canonical hero gradient — used in app HomeView, app PaywallView, web hero, web footer) |
| Brand violet | `#7C3AED` (primary accent — wordmark glow, key chrome) |
| Brand cyan | `#0EA5E9` (secondary accent — highlights, target glow) |
| Brand white | `#FFFFFF` (glyph + type on dark) |
| Annotation accent (product only) | `#FF3B30` iOS systemRed — the in-app walkthrough circle. Used on web only for that motif. |
| Primary typeface | **System font stack** — `-apple-system, BlinkMacSystemFont, "SF Pro Display", "SF Pro Text", "Helvetica Neue", system-ui, sans-serif` |
| Pro Monthly | **$4.99 / month**, 7-day free trial |
| Pro Annual | **$49.99 / year**, no trial |
| Topic Pack (each) | **$6.99**, one-time, lifetime, Family Sharing on |

---

## 1. Identity

### 1.1 Name
- **TapThrough** — always one word, both T's capitalized.
- Never "Tap Through", "TapThru", "Tap-Through", or "tapthrough" in body copy.
- The wordmark may use uniform case (e.g. all-caps "TAPTHROUGH" in a nav bar) when the surrounding design calls for it; CamelCase is the default.

### 1.2 Tagline (canonical)
> **The fastest way to fix what your iPhone apps are doing.**

Allowed short variants:
- "Fix what your iPhone apps are doing — in 20 seconds."
- "Visual walkthroughs for the settings Apple hides four menus deep."

Do NOT use:
- "Learn your iPhone" / "iPhone tutorials" / "Master your iPhone" — we don't sell education, we sell completion.
- "AI for your iPhone" — we are not an AI product.

### 1.3 Operator
- Legal name: **Jedrock LLC** (a California limited liability company).
- Trade name: TapThrough.
- TapThrough is a product of Jedrock LLC and is **not affiliated with, endorsed by, sponsored by, or partnered with** Apple Inc. or any third-party app shown in our walkthroughs.

### 1.5 Audiences and how to write to each one

Per `.planning/VISION.md` §"Target users (initial wedge)", TapThrough has five distinct target audiences with one shared pain (hidden settings, outdated tutorials, confusing interfaces) but very different vocabularies, motivations, and lead hooks. Every marketing surface should be reviewed against this list to make sure it speaks to more than one.

| # | Audience | Lead hook | Primary pack | Sample headline copy |
|---|---|---|---|---|
| 1 | **Older adults & less tech-savvy users** | Comfort + clarity. "You're not failing; iOS moved it." | Display & Accessibility, Battery & Storage | "If your iPhone feels harder than it should." |
| 2 | **Parents managing kids' devices** | Safety + control. "Set it up right the first time." | Family Safety | "If you're setting up your kid's first phone." |
| 3 | **Privacy-conscious adults** | Reveal + take-back. "Defaults betrayed you. Fix them." | Privacy | "If your apps know more about you than you do." (= current hero) |
| 4 | **Switchers** (Android→iOS, major iOS upgrade) | Speed + relief. "Find anything Apple moved." | Free tier + onboarding walkthroughs | "If you just got a new iPhone." |
| 5 | **General iPhone users** wanting time/money savings | Specific outcomes + ROI. "Cancel Prime in 30 seconds." | Time & Money Savers | "The fixes that pay for the app in the first week." |

**Lead hook formats per audience** (from `content-strategy.md` §1a):
- The **Reveal** (privacy-conscious) — cold-open with a threat, walkthrough fixes it, end card.
- The **Race** (savers, switchers) — split-screen "fumbling vs. tap-tap-done," ends with the time gap.
- The **Parent PSA** (parents, older adults) — direct-address parent voice: "If your kid has Snapchat, do this tonight."

**Authoring rule for any marketing surface:**
1. Identify the audience the surface is for (write it in a comment if it's not obvious).
2. Use that audience's vocabulary, not the others'. ("Screen Time," "TikTok Family Pairing" for parents; "find anything," "Wi-Fi setup" for switchers; "broadcasting," "default settings" for privacy.)
3. If the surface is the homepage or App Store description (broad audience): include language that speaks to at least 3 of the 5 above, not just one. The current homepage's "Who it's for" section is the canonical example.
4. Never collapse all audiences into one vague tagline. ("Helps with iPhone settings" speaks to nobody.)

---

### 1.4a Privacy positioning (use this framing — not over-claims, not defensive lists)

TapThrough's privacy story is **"you're not the product."** Stated once, calmly. Our customers are regular people, not security researchers — they want to know they can trust us, not read a hostage statement.

**Voice rules for any privacy-adjacent copy:**
- **Short.** Two or three sentences on a marketing surface. Long enough that the legal policy can be specific; short enough that the marketing site doesn't feel defensive.
- **Calm.** Don't enumerate vendors we don't use. Don't list SDK names. Don't pre-emptively defend against accusations no one is making.
- **No jargon.** No "IDFA," no "SDK," no "behavioral profile," no "data broker" on marketing surfaces. Plain language only.
- **One idea per surface.** The homepage says one thing about privacy; the policy says the detail.

**Marketing-surface examples (use this voice):**
> Headline: "We don't sell your data."
> Body: "Your subscription is how we get paid. You'll never see an ad, and the little we measure is anonymous — just enough to make the app better."

**Headline rules:** lead with the clearest plain-English statement of the promise. "We don't sell your data" is what a 60-year-old grandparent understands on first read. Avoid headlines that require knowing the industry-insider phrase "you're not the product" — that's a tell that the writer is talking to a product team, not to a real person.

**Wrong framing — DO NOT USE on marketing surfaces:**
- "We collect zero data." (over-claim — App Store Connect gives us aggregate analytics by default)
- "Zero analytics SDKs forever." (over-claim — privacy-respecting analytics like Aptabase / TelemetryDeck are likely future additions and there's no shame in that)
- "We don't integrate tracking SDKs from Google, Meta, or any ad network." (defensive — names vendors no regular person is asking about)
- "No IDFA." (jargon — readers don't know what this is)
- Enumerated lists of specific things we don't do, on marketing surfaces. (Goes in the policy. Not the homepage.)

**Privacy Policy ≠ marketing copy.** The full Privacy Policy (`tapthrough-site/privacy.html`) is the right place for specific vendor names, SDK lists, and enumerated commitments — that's the policy genre, and the audience reading it expects detail. The homepage, App Store description, social posts, and press lines stay in the calm-and-short voice above.

**What we DO collect (current and anticipated):**
- Aggregate, anonymous App Store Connect analytics that Apple gives us by default (install counts, country breakdowns, revenue, aggregate crash counts).
- iOS system-level crash diagnostics if the user has opted in at the OS level.
- StoreKit purchase receipts (anonymous, required to unlock paid content).
- **Likely future**: a privacy-respecting product-analytics service (Aptabase, TelemetryDeck, or equivalent) for anonymous event counts — which walkthroughs are opened most, where users drop off, etc. No cookies. No personal IDs. No cross-app or cross-site tracking. To be disclosed in the privacy policy the moment it ships, including the specific vendor.

**What we will NEVER do (these promises are durable and honest):**
- Sell or share data with data brokers.
- Share data with advertising networks.
- Integrate third-party ad-tech SDKs (Google Analytics, Firebase, Facebook/Meta SDK, AppsFlyer, Adjust, Branch, Mixpanel for ads, etc.).
- Use Apple's Identifier for Advertisers (IDFA).
- Build a behavioral profile tying activities to your identity.
- Show advertisements in the app.
- Use your in-app data to train AI models without explicit, opt-in consent.

**Reference sections that must use this framing:**
- Homepage privacy callout (`tapthrough-site/index.html`)
- Privacy Policy (`tapthrough-site/privacy.html`) — full §2 + §4
- Terms of Service TL;DR (`tapthrough-site/terms.html` §"Short version")
- Any App Store Connect "App Privacy" disclosures
- Future App Store screenshots that lean on privacy positioning
- Future press / launch copy

### 1.4 Trademark line (use verbatim wherever required)
> &copy; 2026 Jedrock LLC. TapThrough is a product of Jedrock LLC, not
> affiliated with or endorsed by Apple Inc. or any third-party app shown in
> our walkthroughs. iPhone, iOS, App Store, and all related marks are
> trademarks of Apple Inc., registered in the U.S. and other countries.

---

## 2. Voice

### 2.1 Tone
Direct. Confident. A little confrontational. Anti-corporate. Plain English.
Sentence-level, not paragraph-level. Funny when it lands; never cute when
it doesn't.

### 2.2 The hook formula
All marketing copy follows: **Threat + Speed + Proof.**

> "Your [app] is doing [bad thing]. Fix it in [N seconds]. Watch."

Examples that work:
- "Strangers can see your Venmo payments. Fix it in 20 seconds. Watch."
- "Snapchat is broadcasting your location. Turn on Ghost Mode in four taps."
- "Google has every place you've been since 2014. Delete it all in one tap."

### 2.3 Do / Don't
| Do | Don't |
|---|---|
| Name the threat specifically. | "Improve your privacy." |
| Cite the time it takes. | "Quick and easy." |
| Use plain verbs: fix, stop, turn off. | "Enhance," "optimize," "leverage." |
| Address the reader directly: "you," "your." | "Users will find that…" |
| Keep sentences short. | Run-on disclaimer paragraphs. |
| Say "iPhone." | "Mobile device," "smartphone." |

---

## 3. Typography

### 3.1 Primary stack (web)
```css
font-family:
  -apple-system,
  BlinkMacSystemFont,
  "SF Pro Display",
  "SF Pro Text",
  "Helvetica Neue",
  system-ui,
  sans-serif;
```

**Rationale:** TapThrough is an iPhone-only app. The iPhone renders this app
in SF Pro by default. The website must feel like a continuation of the app on
the same device — so the website renders in SF Pro by default on every Apple
device. On Windows the stack falls back to Segoe; on Android to Roboto.
Acceptable cross-platform drift, and zero external font requests (matches our
"we don't track you" infrastructure ethos).

**Never use:** Fraunces, Geist, Inter, Roboto, Arial, Helvetica as a single
font, any web-served font, any serif typeface anywhere.

### 3.2 iOS app
The SwiftUI default `Font` is SF Pro. **Do not override.** All `Font.system(…)`
calls in the app use the SF Pro family automatically. No custom font registrations.

### 3.3 Type scale (web)
| Token | Size (clamp) | Weight | Tracking | Use |
|---|---|---|---|---|
| `--t-display` | clamp(48px, 8vw, 96px) | 700 | -0.025em | Hero only |
| `--t-title-1` | clamp(36px, 4.5vw, 56px) | 700 | -0.02em | Section titles |
| `--t-title-2` | clamp(24px, 2.5vw, 32px) | 600 | -0.015em | Card titles, threat headlines |
| `--t-headline` | 20px | 600 | -0.01em | Sub-section headings |
| `--t-body-large` | clamp(17px, 1.4vw, 21px) | 400 | 0 | Lede paragraph |
| `--t-body` | 17px | 400 | 0 | Body copy |
| `--t-callout` | 16px | 500 | -0.005em | UI buttons, prices |
| `--t-footnote` | 13px | 400 | 0 | Fine print |
| `--t-caption` | 12px | 500 | 0.04em | Eyebrows (uppercased) |

Line-height: 1.05 for display, 1.15 for title-1/2, 1.5 for body, 1.4 for callout/footnote.

### 3.4 No italics for emphasis
SF Pro italics exist but read as "system label." Emphasize with **weight** or
with **color** (the brand red), never with `<em>` styling on body copy.

---

## 4. Color

### 4.1 Two color systems — brand and annotation

TapThrough operates with two separate color systems that must not be confused.

- **Brand system** — the icon, the dark hero, the wordmark surroundings. Deep violet gradient + pure white + teal target dot. This is what the user remembers as "the look of TapThrough."
- **Annotation system** — the in-app red circle drawn around every "tap here" target. iOS systemRed. The product mechanic itself. Used on the web only for that specific motif (the hand-drawn circle), never as a section bg, never as primary chrome.

### 4.2 Brand tokens (the dark violet identity — adopted verbatim from the iOS app's prior art in `HomeView` and `PaywallView`)

The hex values below are LOCKED. They match the existing iOS app exactly so the app and the web surface are pixel-identical. Do not adjust without auditing every consumer.

| Token name (CSS) | Token name (Swift) | Hex | Use |
|---|---|---|---|
| `--b-dark-1` | `Brand.darkBase` | `#0D0D1A` | Hero gradient stop 1 (deepest, near-black violet) |
| `--b-dark-2` | `Brand.darkMid` | `#1A1033` | Hero gradient stop 2 (mid violet) |
| `--b-dark-3` | `Brand.darkBlue` | `#0F2044` | Hero gradient stop 3 (cooler navy violet) |
| `--b-violet` | `Brand.violet` | `#7C3AED` | Primary brand accent (wordmark icon tint, key UI chrome, selected states) |
| `--b-cyan` | `Brand.cyan` | `#0EA5E9` | Secondary brand accent (highlights, glows, target-dot color) |
| `--b-white` | `Brand.white` | `#FFFFFF` | Type + glyphs on dark surfaces |
| `--b-white-80` | `Brand.white80` | rgba(255, 255, 255, 0.80) | Soft text on dark |
| `--b-white-55` | `Brand.white55` | rgba(255, 255, 255, 0.55) | Muted text on dark (matches the app's HomeView subtitle opacity) |
| `--b-white-35` | `Brand.white35` | rgba(255, 255, 255, 0.35) | Tertiary text on dark |
| `--b-white-15` | `Brand.white15` | rgba(255, 255, 255, 0.15) | Hairline borders on dark |
| `--b-violet-glow` | `Brand.violetGlow` | rgba(124, 58, 237, 0.35) | Diffused violet glow (HomeView decorative blob) |
| `--b-cyan-glow` | `Brand.cyanGlow` | rgba(14, 165, 233, 0.25) | Diffused cyan glow (HomeView decorative blob) |

### 4.3 Surface tokens (light sections of the site + app body)
| Token | Light | Dark | Use |
|---|---|---|---|
| `--c-bg` | `#FFFFFF` | `#000000` | Light page background / iOS dark base |
| `--c-bg-2` | `#F5F5F7` | `#1C1C1E` | Card surfaces, dividers |
| `--c-ink` | `#1D1D1F` | `#F5F5F7` | Primary text on light |
| `--c-ink-2` | `#424245` | `#A1A1A6` | Secondary text |
| `--c-muted` | `#6E6E73` | `#86868B` | Tertiary text |
| `--c-rule` | `#D2D2D7` | `#3A3A3C` | Hairlines |

### 4.4 Annotation token (the in-app red circle)
| Token | Light | Dark | Use |
|---|---|---|---|
| `--a-red` | `#FF3B30` | `#FF453A` | The hand-drawn circle motif. Tap-target color. |
| `--a-red-soft` | rgba(255, 59, 48, 0.10) | rgba(255, 69, 58, 0.16) | Subtle red wash, the pulsing dot's halo. |

### 4.5 Pack accent colors (cards, badges, future pack-pages)
Each pack gets a signature gradient. Used on the pack card on the website AND on the in-app pack header. Hex values are adopted from `TapThrough/Extensions/CategoryStyle.swift` where the app already uses them (currently keyed by category — to be re-keyed by pack in the Phase-D rename, see §11.2).

| Pack | Gradient (start → end) | Swift constants | Anchored in |
|---|---|---|---|
| Lock Down Your Privacy | `#7C3AED → #4F46E5` | `Brand.Pack.privacy` | Brand violet → indigo |
| Family Safety | `#0EA5E9 → #0284C7` | `Brand.Pack.family` | Trust blue |
| Time & Money Savers | `#EA580C → #D97706` | `Brand.Pack.savers` | Urgent orange |
| Battery & Storage | `#10B981 → #059669` | `Brand.Pack.battery` | Healthy green |
| Display & Accessibility | `#4F46E5 → #6D28D9` | `Brand.Pack.display` | Indigo → violet |
| Cross-App / Pro | `--b-dark-2 → --b-dark-1` with `--b-violet` glow | `Brand.Pack.pro` | Pure brand dark, premium |

All pack gradients are linear, top-left to bottom-right, 135°.

### 4.6 Annotation-color discipline
The `--a-red` token appears in **three** places, and only three:

1. The hand-drawn circle motif on the web (echoes the in-app annotation).
2. The pulsing "coming soon" dot in the eyebrow.
3. The "BEST VALUE" pricing tag.

Red is **never** used for body text, never as a section background, never
in gradients other than the soft halo. It earns its emphasis by scarcity.

---

## 4.7 The App Icon — the most permanent brand asset

The 1024×1024 icon is the single longest-lived brand artifact (it lives on every customer's home screen). Treat it as the source of truth for the brand palette, and use it visibly on every surface.

### 4.7.1 Description
A white glowing index-finger silhouette in a tapping gesture against a deep violet radial gradient. A teal/blue target dot sits above the finger to indicate the tap target. The white glyph has a soft cyan glow halo, suggesting the moment of contact.

### 4.7.2 File locations
- **Master**: `TapThrough/Assets.xcassets/AppIcon.appiconset/AppIcon-1024.png` (1024×1024 PNG)
- **Web mirror**: `tapthrough-site/img/icon.png` — identical file, copied to the website repo. Re-sync any time the master changes.

### 4.7.3 Web usage rules
- Use as `<link rel="icon">` and `<link rel="apple-touch-icon">` on every page.
- Show prominently in the homepage hero (≥120px display size).
- Show in the footer near the wordmark (≤56px display size).
- Never recolor, never alter the proportions, never crop the rounded square frame.
- If displaying on a non-dark background, add a subtle drop shadow `0 8px 24px rgba(19, 7, 58, 0.25)` so the violet halo doesn't disappear.

### 4.7.4 In-app usage
The icon is the app icon — no further app-internal usage required. The brand wordmark inside the app uses SF Pro Display Bold, not the icon.

---

## 5. The Red Circle (signature motif)

The product itself draws a red circle around every "tap here" target in every
walkthrough. That circle is the brand. It appears on the website as a recurring
visual element wherever the design needs to point at something.

### 5.1 Visual spec
- **Shape**: slightly imperfect ellipse, drawn as if with a fine marker.
- **Stroke**: 3px on web display sizes, scaled proportionally smaller for body sizes.
- **Color**: `--c-red`.
- **Cap**: round.
- **No fill.**
- **Hand-drawn feel**: the path should have slight asymmetry. Geometric perfect circles look corporate; ours look human.

### 5.2 SVG (canonical path)
```html
<svg viewBox="0 0 240 70" preserveAspectRatio="none" aria-hidden="true">
  <path d="M 14 36 C 18 12, 60 6, 122 7 C 188 9, 230 19, 228 38
           C 226 56, 178 65, 110 64 C 50 63, 10 56, 14 36 Z"
        fill="none" stroke="currentColor" stroke-width="3" stroke-linecap="round" />
</svg>
```

### 5.3 Motion
On page load: stroke draws in over ~1.1s with a slight ease-out. One signature
moment per page. Honor `prefers-reduced-motion`.

### 5.4 Where to use
- Around the time-to-fix phrase in any hero ("20 seconds").
- Around the canonical CTA ("Watch").
- Around a single-word concept in a section eyebrow.
- Around a price you want to emphasize ("$6.99").

**Limit one per visible viewport.** If you'd circle three things, you'd circle nothing.

---

## 6. Pricing — single source of truth

| Product ID | Display name | Price (US) | Trial | Renews | Family Sharing | Group |
|---|---|---:|---|---|---|---|
| `org.jedrock.tapthrough.pro.monthly` | **Pro Monthly** | $4.99 | 7 days | Monthly auto-renew | Off | TapThrough Pro |
| `org.jedrock.tapthrough.pro.annual` | **Pro Annual** | **$49.99** | none | Yearly auto-renew | Off | TapThrough Pro |
| `org.jedrock.tapthrough.pack.privacy` | **Lock Down Your Privacy** pack | $6.99 | n/a | One-time, lifetime | On | (non-consumable) |
| `org.jedrock.tapthrough.pack.kidsiphone` | **Family Safety** pack | $6.99 | n/a | One-time, lifetime | On | (non-consumable) |
| `org.jedrock.tapthrough.pack.savers` | **Time & Money Savers** pack | $6.99 | n/a | One-time, lifetime | On | (non-consumable) |
| `org.jedrock.tapthrough.pack.battery` | **Battery & Storage** pack | $6.99 | n/a | One-time, lifetime | On | (non-consumable) |
| `org.jedrock.tapthrough.pack.display` | **Display & Accessibility** pack | $6.99 | n/a | One-time, lifetime | On | (non-consumable) |

### 6.1 Derived math
- **Annual equivalent monthly**: $49.99 / 12 ≈ **$4.17 / month** (round to two decimals; surface as "~$4.17/mo equivalent" or omit on tight surfaces).
- **Annual savings vs. monthly**: 12 × $4.99 = $59.88; ($59.88 − $49.99) / $59.88 = **16.5%**. Round to **"Save ~17%"** or **"Save ~16%"** depending on rounding house style. Choose one and stick to it; this doc picks **17%**.
- **Pack vs. Pro Annual**: one $6.99 pack = 14% of a $49.99 Pro Annual. Five packs together would cost $34.95 — a Pro Annual buys ~43% more (Pro-exclusive workflows + all future packs) for $15.04 more.

### 6.2 Required Apple disclosure (use verbatim in Terms + paywall)
- Payment will be charged to your Apple ID account at confirmation of purchase.
- Your subscription automatically renews unless auto-renew is turned off at least 24 hours before the end of the current period.
- Your account will be charged for renewal within 24 hours prior to the end of the current period at the price of the plan you selected.
- You can manage your subscriptions and turn off auto-renewal by going to Settings &rarr; your Apple ID &rarr; Subscriptions.
- Any unused portion of a 7-day free trial, if offered, will be forfeited when you purchase a subscription before the trial ends.

### 6.3 Surfaces that must align
| Surface | File / location |
|---|---|
| Website pricing card | `tapthrough-site/index.html` |
| Website Terms §4 | `tapthrough-site/terms.html` |
| iOS app paywall | `TapThrough/Views/PaywallView.swift` (locale-aware via StoreKit) |
| StoreKit sandbox config | `TapThrough/TapThrough.storekit` |
| App Store Connect | _Pending registration; the user enters prices here directly_ |
| Monetization spec | `.planning/MONETIZATION.md` |
| Content strategy | `.planning/content-strategy.md` |
| MVP plan | `.planning/MVP_PLAN.md` |
| UX plan | `.planning/UX_PLAN.md` |
| Project status snapshot | `.planning/PROJECT.md` |

Any of those references that says `$39.99` or `$3.33` is stale. The
2026-05-15 price correction is THE event that ratifies §6.

---

## 7. Layout principles (web)

1. **Light mode is the canonical surface.** Dark mode is supported (system-trigger) but design decisions are made against white.
2. **Generous whitespace.** Aim for sections that breathe: minimum 96px vertical padding between sections, more on the hero.
3. **Max content width 1180px.** Inner text columns cap at ~64ch for readability.
4. **No drop shadows.** Use hairline borders (`--c-rule`) instead. Apple's product pages use almost no shadows; we follow.
5. **No rounded-everything.** Cards have 18px radius; pills have full radius; buttons match cards. Inline elements (links, badges) stay sharp.
6. **One CTA per section.** Mailto, App Store link, or Read More — never two competing CTAs in the same viewport.
7. **Image > illustration > emoji.** If we ever ship illustrations, they're product screenshots; emoji are never the brand.

---

## 8. App ↔ Web parity contract

Whenever either surface ships a user-facing change that the other surface references, both must move together.

| Topic | If you change it, also update |
|---|---|
| Pricing | §6 of THIS doc + `TapThrough.storekit` + paywall copy + Terms §4 + website pricing card |
| Brand color | §4 of THIS doc + `Color.brandRed` (or equivalent) in the app + `--c-red` in `tapthrough-site/style.css` |
| Tagline | §1.2 of THIS doc + App Store Connect "subtitle" + website hero |
| Trademark line | §1.4 of THIS doc + every footer (web + in-app About) |
| Trial length | §6 + every paywall, the website pricing card, Terms §4.2 |
| Pack list | §6 + website packs section + in-app pack picker + content-strategy.md |

If any of these moves out of step, the SKU mismatch (or worse, the legal misrepresentation) becomes the next bug.

---

## 9. Surfaces that must include certain elements

### 9.1 Every web page
- `<meta name="viewport" content="width=device-width, initial-scale=1">`
- `<link rel="canonical">` to the public URL
- `<meta name="theme-color">` matched to `--c-bg` (light + dark)
- Trademark line in the footer (§1.4)
- Privacy + Terms links in the footer

### 9.2 Every paywall and pricing surface (app + web)
- All three SKU prices visible at the same level of prominence (per Apple guideline 3.1.2(a))
- The 7-day free trial language only on Pro Monthly
- A link to the full Terms of Service
- A link to the full Privacy Policy
- The Apple-required auto-renewal disclosure (§6.2)

### 9.3 Every in-app screen that references the brand
- The wordmark uses `--c-ink` color (never red — red is reserved for accents)
- Walkthrough annotation circles use exactly `--c-red`, stroke 7pt (iOS), 3pt (web)

---

## 10. Change protocol

To change anything in this doc:

1. Open a commit titled `canonical: <one-line change>`.
2. Update §0 (Quick reference) AND the relevant deep section.
3. In the same commit, update every downstream surface listed in §6.3 or §8 that depends on the value you changed.
4. Tag the commit body with `Canonical-Bump: yes` so future Claude sessions know to re-read this file.

The integrity of `CANONICAL.md` is what keeps drift from happening across the
many places a fact like "Pro Annual is $49.99" lives. Treat updates to this
file as schema migrations: deliberate, paired with downstream propagation,
and committed atomically.

---

## 11. App alignment status & migration plan

The iOS app pre-dates this canonical doc by months. The brand identity in CANONICAL §4 was reverse-engineered from the app's existing visual identity, so most app surfaces are already canonical-compatible. This section tracks the explicit gaps and the migration plan to close them.

### 11.1 Canonical-compatible (no action needed)

| Surface | File | Notes |
|---|---|---|
| App icon | `Assets.xcassets/AppIcon.appiconset/AppIcon-1024.png` | Master source for the brand palette. |
| HomeView hero gradient | `Views/Home/HomeView.swift:114` | Uses `#0D0D1A → #1A1033 → #0F2044` — matches CANONICAL §4.2 exactly. |
| HomeView glow blobs | `Views/Home/HomeView.swift:121,126` | Uses `#7C3AED@35%` + `#0EA5E9@25%` — matches CANONICAL `--b-violet-glow` / `--b-cyan-glow`. |
| PaywallView gradient | `Views/Home/PaywallView.swift:96` | Same gradient triple. |
| Annotation red | rendering in `WalkthroughView` / `AnnotationCircle` | `#FF3B30` — matches CANONICAL §4.4. |
| Typography | every `.font(.system(...))` call | SwiftUI defaults to SF Pro — matches CANONICAL §3.2. |

### 11.2 Drift to fix (prioritized)

| # | Surface | Current state | Canonical state | Priority | Effort |
|---|---|---|---|---|---|
| D-1 | Brand colors are hard-coded `Color(hex: "...")` strings in 46 places | Magic numbers, drift-prone, no single source | All colors route through `Brand.swift` named tokens | **P0** | M (~1h: create file + grep-replace) |
| D-2 | HomeView tagline | `"Learn any app, one step at a time."` | `"The fastest way to fix what your iPhone apps are doing."` (CANONICAL §1.2) | **P0** | XS (1 line) |
| D-3 | HomeView in-app brand mark | `Image(systemName: "hand.tap.fill")` next to the wordmark | The actual app icon (added as a separate `BrandMark` image set so SwiftUI can load it) | P1 | S (~30min: add asset + 2-line view edit) |
| D-4 | `CategoryStyle.swift` keyed by old category names | "Display & Text", "Wireless", etc. | Re-keyed by `PackID` (privacy, family, savers, battery, display) per CANONICAL §4.5 | P1 | M (~1h: rename + map old categories → new packs; update consumers) |
| D-5 | PaywallView Pro Annual price displayed via StoreKit | StoreKit shows whatever ASC has; ASC product unregistered as of 2026-05-15 | Once registered: $49.99 (CANONICAL §6) | **P0 at submit time**, P3 today | N/A locally — App Store Connect action |
| D-6 | In-app About / footer trademark line | Not yet built (no About screen ships in v1.0) | When About lands, footer must include CANONICAL §1.4 verbatim | P2 | S |
| D-7 | Walkthrough player respects forced light mode (per `.claude/rules/ux.md`) | ✅ Already correct — `.preferredColorScheme(.light)` is in place | No action | — | — |
| D-8 | App-side legal URLs | `LegalURLs.swift` constants → `tapthrough.app/privacy` + `/terms` | ✅ Already correct, points at live web pages | — | — |

### 11.3 Migration sequence

1. **This session**: D-1 (Brand.swift) + D-2 (tagline) + sync website CSS to the locked canonical hex values. These are quick, high-impact, and unblock all subsequent drift fixes by giving the codebase a single source of truth for brand colors.
2. **Next session**: D-3 (in-app brand mark using actual icon) + D-4 (CategoryStyle → PackStyle rename).
3. **At App Store Connect product registration**: D-5 (set $49.99 on `pro.annual`).
4. **When v1.0 About screen ships**: D-6 (trademark line in About footer).

### 11.4 Authoring rule for any new app surface

Any new `View` added to the app from this point forward MUST:

- Reference colors via `Brand.*` named tokens — no new `Color(hex: "...")` strings.
- Reference the tagline via `Brand.tagline`, not an inline literal.
- Reference legal URLs via `LegalURLs`, not inline strings.
- Reference product IDs via `SubscriptionConstants.ProductID`, not inline strings.

Adding a new `Color(hex: ...)` literal to a shipping view requires a comment explaining why it cannot use a `Brand.*` token. If you can't write that comment, the right answer is to add a new token to `Brand.swift`.
