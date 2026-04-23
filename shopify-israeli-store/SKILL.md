---
name: shopify-israeli-store
description: Build a complete, high-converting, innovative-looking Shopify ecommerce store for the Israeli market. Use this skill whenever the user wants to create, launch, redesign, or improve a Shopify store in Hebrew for Israeli customers — including homepage, product pages, collection pages, about page, checkout, email flows, Liquid/HTML/CSS code, Hebrew copywriting, RTL layout, Israeli payment methods (Bit, Apple Pay, credit cards, installments), shipping setup (דואר ישראל, שליחים, נקודות איסוף), trust signals, conversion rate optimization, upsells, abandoned cart flows, popups, or marketing automation. Also trigger on phrases like "אני רוצה לפתוח חנות", "אתר שופיפיי", "להעלות חנות אונליין", "לבנות אתר מכירות", "דף נחיתה למוצר", "איך לשפר המרות", "חנות בעברית", "אתר ישראלי", "דרופשיפינג", "איקומרס", "להקים מותג". Even if the user just says "עזור לי למכור X אונליין" or "אני רוצה שהאתר שלי ייראה יותר מקצועי" — use this skill.
---

# Shopify Israeli Store Builder

A complete framework for building high-converting, design-forward Shopify stores for the Israeli market. This skill produces the **entire store** — strategy, design direction, Hebrew copy, Liquid/HTML/CSS code snippets, and marketing automation — not just one piece.

## Core philosophy

This skill is built around **three non-negotiable principles**:

1. **Conversion first, beauty second** — every design choice must be justified by how it affects the purchase decision. "Looks cool" is not a reason.
2. **Israeli-native, not Google-translated** — everything is built for Israeli buyers from the ground up: RTL, Hebrew that sounds native (not translated), local payment methods, local trust signals, local shipping, local tone.
3. **Distinctive, not generic** — the user explicitly wants the store to look "חדשני, מיוחד ושונה". Avoid the template Shopify look. Lean into editorial, bold, and opinionated design.

## Workflow: The Fast Mode

The user chose the fast execution style. Do NOT ask 20 discovery questions. Instead:

### Step 1 — Minimal Discovery (5 questions, max)

Ask these questions in one message, compactly. Use Hebrew in all user-facing communication:

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

Based on the answers, deliver in a single response:

1. **אסטרטגיית מותג** (3-4 שורות) — positioning, tone of voice, what makes this store different
2. **פלטת עיצוב** — primary color, secondary, accent, background, text. With hex codes. Justify each choice.
3. **טיפוגרפיה** — 2 fonts max: one for headlines (distinctive, bold), one for body. Hebrew-first fonts. Recommend specific fonts from Google Fonts that support Hebrew well.
4. **מבנה דפי האתר** (sitemap) — every page with its purpose
5. **Next step recommendation** — which page to build first (always recommend product page first — it's where conversion happens)

### Step 3 — Build each page on demand

After the plan, the user picks what to build. For each page, load the relevant reference file:

- **Homepage** → `references/homepage-blueprint.md`
- **Product page** → `references/product-page-blueprint.md` ⭐ (the most important page)
- **Any page, Hebrew copy** → `references/hebrew-copywriting.md`
- **Anything about the Israeli market** → `references/israeli-market.md`

Each page delivery must include:
- **Section-by-section structure** (what appears, in what order)
- **Hebrew copy** ready to paste (headlines, body, CTAs, microcopy)
- **Design direction** (layout, spacing, imagery guidance)
- **Liquid code snippets** when they add value (especially for dynamic elements)
- **Why it converts** (brief explanation under each section — this teaches the user)

## Critical rules (never break these)

### Hebrew copywriting rules

- **Never** use translated-English phrasing. "הוסף לעגלה" is fine; "הוסף לסל הקניות שלך" sounds like Google Translate.
- **Always** write in a natural, direct Israeli tone — short sentences, a little cheeky, not formal.
- **Never** write "אנחנו מאמינים ש..." or "המשימה שלנו היא..." — this is corporate nonsense that converts nobody.
- **Prefer** second-person singular ("אתה", "את", "שלך") over plural. It's more personal.
- **CTAs are short and verb-first**: "תתחיל עכשיו", "קנה היום", "אני רוצה", "שלח לי". Never "לחץ כאן".

### Design rules

- **Default to distinctive**: if a design choice is "safe" and used by every Shopify store, push for something more interesting. The user explicitly wants "חדשני ושונה".
- **Typography does heavy lifting**: the user wants the site to look premium. Large, confident type is the single fastest way to achieve this. Recommend display-weight fonts for headlines.
- **Whitespace is a feature, not an absence**: premium feels = generous spacing.
- **Motion should be intentional**: recommend scroll-triggered reveals, hover states, but never auto-playing carousels (kill conversion).
- **Mobile-first always**: 85%+ of Israeli ecommerce traffic is mobile. Every layout decision gets made for a 375px screen first, then scaled up.

### Israeli market non-negotiables

- **RTL is mandatory** — Shopify supports this; instruct the user to use a theme that handles RTL natively (Dawn works, some premium themes are better).
- **Payment methods to enable (in order of importance):**
  1. כרטיסי אשראי (via Shopify Payments or tranzila/Pelecard)
  2. ביט — huge in Israel, many younger customers prefer it
  3. Apple Pay / Google Pay
  4. PayPal
  5. תשלומים (installments) — significantly improves conversion, especially for items over 300₪
- **Always show prices with VAT included** — showing price without VAT and adding it at checkout destroys trust in Israel.
- **Shipping must be explicit and upfront** — Israelis hate surprises at checkout more than most markets. Show delivery time clearly (e.g., "משלוח תוך 2-3 ימי עסקים").
- **WhatsApp is king for support** — recommend a floating WhatsApp button; it's a trust multiplier in Israel.

### Conversion rules

- **Free shipping threshold** — always recommend one. The psychology of "עוד 40 שקלים למשלוח חינם" is the single most effective upsell mechanism.
- **Urgency must be honest** — never fake countdown timers. Real stock levels ("נשארו 4 יחידות"), real shipping cutoffs ("הזמן בשעה הקרובה וקבל היום") only.
- **Social proof is oxygen** — every page needs it. Reviews with photos > reviews without > star ratings alone.
- **Reduce friction obsessively** — guest checkout, autofill, address by postal code, saved payment methods.

## Deliverable format

When producing a full page (homepage, product page, etc.), structure the output like this:

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

## When uncertain

- If the user's answers in Step 1 are vague, don't ask 10 follow-ups. Make confident assumptions, state them, and move forward. The user chose fast mode — respect it.
- If the user asks for something that hurts conversion (e.g., "תעשה דף מוצר עם 20 וריאציות בלי תמונות"), push back briefly and suggest a better approach.
- When recommending external apps (reviews, upsells, SMS), name 2-3 options at different price points; don't pretend there's only one answer.

## Reference files — when to load each

- `references/homepage-blueprint.md` — Load when building the homepage. Contains section-by-section blueprints, hero patterns, and above-the-fold strategies.
- `references/product-page-blueprint.md` — Load when building product pages (highest priority — this is where money is made). Contains the full anatomy, PDP patterns by product type, and the Israeli-specific trust stack.
- `references/israeli-market.md` — Load whenever a question touches payments, shipping, legal, tax, trust signals, or anything Israel-specific.
- `references/hebrew-copywriting.md` — Load before writing any user-facing Hebrew copy. Contains voice guidelines, CTA banks, do/don't phrase lists, and headline formulas.
