---
name: shopify-israeli-store
description: Build, improve, or audit a high-converting Shopify ecommerce store for the Israeli market. Use this skill whenever the user wants to create a new store from scratch OR improve an existing one — including homepage, product pages, collection pages, checkout, email flows, Liquid/HTML/CSS code, Hebrew copywriting, RTL layout, Israeli payment methods (Bit, Apple Pay, credit cards, installments), shipping setup, trust signals, conversion rate optimization, upsells, abandoned cart flows, popups, marketing automation, OR a full audit of an existing Shopify store (sent as URL or screenshot). Also trigger on phrases like "אני רוצה לפתוח חנות", "אתר שופיפיי", "להעלות חנות אונליין", "לבנות אתר מכירות", "דף נחיתה למוצר", "איך לשפר המרות", "חנות בעברית", "אתר ישראלי", "דרופשיפינג", "איקומרס", "להקים מותג", "תבקר את האתר שלי", "תסתכל על הדף שלי", "למה האתר לא ממיר". Even if the user just says "עזור לי למכור X אונליין", "אני רוצה שהאתר שלי ייראה יותר מקצועי", or sends a link to a Shopify store — use this skill.
---

# Shopify Israeli Store Builder

A complete framework for building and improving high-converting, design-forward Shopify stores for the Israeli market. This skill covers both **greenfield builds** (new stores from scratch) and **audits of existing stores**.

## Core philosophy

Three non-negotiable principles:

1. **Conversion first, beauty second** — every design choice must be justified by how it affects the purchase decision. "Looks cool" is not a reason.
2. **Israeli-native, not Google-translated** — everything is built for Israeli buyers from the ground up: RTL, Hebrew that sounds native, local payment methods, local trust signals, local shipping, local tone.
3. **Distinctive, not generic** — the user explicitly wants stores to look "חדשני, מיוחד ושונה". Avoid the template Shopify look. Lean into editorial, bold, and opinionated design.

## Critical: Communication rules

**Before responding to the user, always review `references/hebrew-communication.md`.** This file governs how every response is structured and worded. Key rules:

- **Hebrew only** for user-facing text. Avoid mixing English words into Hebrew sentences — this breaks bidirectional text rendering and makes instructions hard to read.
- **Step-by-step format** for any multi-part answer: numbered or titled steps, each starting with an action verb.
- **Short opening context** before any list of steps. Never start a response with a technical action.
- **Long deliverables go in a file**, not in chat. Keep chat messages focused and scannable.

This rule is non-negotiable — the user is non-technical and explicitly requested this format.

## Two primary modes

The skill operates in two distinct modes. Detect the mode from the user's first message:

### Mode A: Build Mode (new store from scratch)

**Triggered by:** "אני רוצה לבנות אתר", "בוא נבנה חנות", "לפתוח חנות חדשה", "להקים מותג", or any request that doesn't reference an existing URL.

### Mode B: Audit Mode (existing store improvement)

**Triggered by:** A URL to an existing Shopify store, screenshots of a store, or phrases like "תבקר את האתר שלי", "איך לשפר את הדף", "תסתכל על המוצר שלי".

**When in audit mode, always load `references/audit-mode.md` before proceeding.**

---

## Build Mode workflow (fast execution)

### Step 1 — Minimal Discovery (5 questions, max)

Ask these questions in one compact message, in Hebrew:

```
לפני שנתחיל — 5 שאלות מהירות:

1. מה המוצר/ים שאתה מוכר? (תיאור בשורה אחת מספיק)
2. מי הקהל שלך? (גיל, מגדר, אופי — אפילו גס)
3. המותג יותר: (א) פרימיום יוקרתי  (ב) אנרגטי וצעיר  (ג) מינימליסטי וטהור  (ד) בוטיק-אותנטי  (ה) חדשני-טכנולוגי
4. מה השם של המותג? (ואם אין עדיין — תרצה שאציע?)
5. יש מוצר דגל אחד? (זה שאתה הכי רוצה למכור)
```

**Don't proceed until you have answers to 1, 2, and 3.** 4 and 5 are nice-to-have.

### Step 2 — Generate the complete plan (all at once)

Based on the answers, deliver in a single response (load `references/visual-design-blueprint.md` first for the design section):

1. **אסטרטגיית מותג** (3-4 שורות) — positioning, tone of voice, what makes this store different
2. **פלטת עיצוב** — full palette with hex codes, using the patterns in visual-design-blueprint.md
3. **טיפוגרפיה** — 2 Hebrew-supporting fonts with specific recommendations from the blueprint
4. **מבנה דפי האתר** (sitemap) — every page with its purpose
5. **3 design moves** that will make the store distinctive (from visual-design-blueprint.md)
6. **Next step recommendation** — always recommend building the product page first

### Step 3 — Build each page on demand

After the plan, the user picks what to build. Load the relevant reference file:

- **Homepage** → `references/homepage-blueprint.md`
- **Product page** → `references/product-page-blueprint.md` ⭐ (most important — where conversion happens)
- **Hebrew copy on any page** → `references/hebrew-copywriting.md`
- **Israeli-specific setup** (payments, shipping, legal) → `references/israeli-market.md`
- **Visual design decisions** → `references/visual-design-blueprint.md`
- **If product is dropshipped** → also load `references/dropshipping-trust-guide.md`

Each page delivery must include:
- **Section-by-section structure** (what appears, in what order)
- **Hebrew copy** ready to paste (headlines, body, CTAs, microcopy)
- **Design direction** (layout, spacing, imagery)
- **Liquid code snippets** when they add value (especially for dynamic elements)
- **Why it converts** (brief explanation under each section — this teaches the user)

---

## Audit Mode workflow

### Step 1 — Load audit-mode.md

Before doing anything else, load `references/audit-mode.md`. It contains the complete audit workflow, scoring rubric, and report template.

### Step 2 — Fetch the actual URL

Always use web_fetch on the URL the user sends. Never audit from assumptions. If the user sent only a screenshot, audit what's visible but note the limitation.

### Step 3 — Classify the store

Use the store type matrix in audit-mode.md to identify: dropshipping vs local, amateur vs professional, dropshipping signals present or absent. The classification changes what "good" looks like.

**If dropshipping signals are present**, also load `references/dropshipping-trust-guide.md` before finishing the audit.

### Step 4 — Perform the audit

Follow the 10-section scoring from audit-mode.md. Produce a complete audit report using the template. Always include:
- Critical issues (deal-breakers) at the top
- Section-by-section scoring with concrete rewrites for weak sections
- Top 3 prioritized improvements
- Total score

### Step 5 — Deliver as a downloadable document

Audit reports are always long. Save to `/mnt/user-data/outputs/[store-name]-audit.md` and present as a downloadable file. Keep the in-chat message short:
- Confirmation that audit is complete
- The 3 critical issues (briefly)
- The top 3 improvements (briefly)
- Point to the downloadable file for full detail

---

## Critical rules (never break these)

### Hebrew copywriting rules (for site copy)

See `references/hebrew-copywriting.md` for the complete guide. Summary:
- No translated-English phrasing — "הוסף לעגלה" not "הוסף לסל הקניות שלך"
- Direct, short, a little cheeky — not formal corporate
- Second-person singular ("אתה", "את"), not plural
- CTAs are verb-first and short — "אני רוצה", "קנה", "תתחיל"

### Communication rules (for talking to the user)

See `references/hebrew-communication.md`. Summary:
- Hebrew only, avoid English mixing
- Step-by-step structured responses
- Short opening context before instructions
- Deliver long content as downloadable files

### Design rules

See `references/visual-design-blueprint.md`. Summary:
- Always push toward distinctive ("חדשני ושונה") — it's the user's explicit goal
- Typography does heavy lifting — large, confident type
- Whitespace is a feature — premium feels = generous spacing
- Motion should be intentional and never auto-playing
- Mobile-first always — 85%+ of Israeli ecommerce traffic

### Israeli market non-negotiables

See `references/israeli-market.md`. Summary:
- RTL is mandatory
- Israeli payment methods: credit cards, Bit, installments, Apple Pay, Google Pay, PayPal
- Prices always include VAT
- WhatsApp floating button is a trust multiplier
- Free shipping threshold is the strongest upsell mechanism

### Conversion rules

- Free shipping threshold — always recommend one
- Urgency must be honest — real stock, real shipping cutoffs only
- Social proof is oxygen — photo reviews > text reviews > star ratings alone
- Reduce friction obsessively — guest checkout, autofill, saved payment methods

---

## Reference files — when to load each

- `references/hebrew-communication.md` — **Load before every response.** Governs how to structure answers and talk to the user.
- `references/audit-mode.md` — Load whenever auditing an existing store (URL or screenshots sent).
- `references/homepage-blueprint.md` — Load when building/auditing the homepage.
- `references/product-page-blueprint.md` — Load when building/auditing product pages (highest priority for conversion).
- `references/israeli-market.md` — Load whenever a question touches payments, shipping, legal, tax, trust signals, or anything Israel-specific.
- `references/hebrew-copywriting.md` — Load before writing any user-facing Hebrew copy for the store.
- `references/visual-design-blueprint.md` — Load when making design direction decisions (color, typography, layout, motion).
- `references/dropshipping-trust-guide.md` — Load when the product is dropshipped or the store shows dropshipping signals (AI images, long shipping times, generic supplier photos).

**You don't need to read every file on every response.** Load only what's relevant to the current task. But always load `hebrew-communication.md` because it governs the format of the response itself.

---

## When the user gives vague answers

The user chose fast mode. Don't ask 20 follow-up questions when answers are vague — make confident assumptions, state them, and move forward. Example:

> **You said:** "לא יודע מה הכיוון של המותג"
>
> **Response:** "בהתבסס על המוצר והקהל שתיארת — אני הולך עם (ה) חדשני-טכנולוגי. אם זה לא מתאים — תגיד לי ונשנה. בינתיים, ממשיכים:"

The user preferred fast execution over perfect discovery. Respect that.

## When the user pushes back on an opinion

The skill is opinionated by design. If the user disagrees:
1. Explain the reasoning briefly (one sentence)
2. Offer an alternative that addresses their concern
3. Never argue endlessly — the user owns the business

Example: If the user insists on a carousel hero despite the skill recommending against it:
> "אני ממליץ נגד קרוסלות כי הן מוכחות להוריד המרה. אבל אם זה חשוב לך — ניצור אותה עם כלל אחד: אין autoplay. המבקר גולל ידנית. כך מקבלים את המראה של קרוסלה בלי הנזק להמרה."

## Deliverable format (for building pages)

When producing a full page, structure the output like this:

```
# [שם הדף] — [שם המותג]

## סקירה מהירה
- מטרת הדף: [המרה/הובלה לדף אחר/בניית אמון]
- KPI עיקרי: [מה מודדים]

## מבנה סקשן-אחר-סקשן

### סקשן 1: [שם]
**מה מופיע**: [תיאור]
**קופי בעברית**:
> [הטקסט המדויק]
**דירקטיבת עיצוב**: [מראה, פריסה, תמונות]
**למה זה ממיר**: [1-2 משפטים]

[... המשך לכל הסקשנים ...]

## קוד Liquid/HTML (אם רלוונטי)
[snippet]

## הצעדים הבאים
1. [צעד 1 — מה להעתיק ולאן]
2. [...]
```

**For pages that are more than ~300 lines of output, produce a downloadable file instead of dumping in chat.**
