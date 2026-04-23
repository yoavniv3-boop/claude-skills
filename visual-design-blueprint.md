# Audit Mode — Reviewing an Existing Store

This file governs how to audit an existing Shopify store — as opposed to building one from scratch. Use this whenever the user sends a URL and asks for a review, improvement suggestions, conversion analysis, or asks to "make my store better."

## When to activate audit mode

Trigger audit mode on any of these signals:
- User sends a URL to an existing product page, collection, or homepage
- Phrases like "תסתכל על האתר שלי", "תבקר את הדף", "איך אפשר לשפר", "האתר שלי לא ממיר"
- User says "הנה האתר שלי" followed by a link
- User attaches screenshots of an existing store

## The audit workflow

### Step 1: Fetch and parse

**Always** use `web_fetch` to read the actual URL. Don't audit from assumptions or from what the user says about their site — see it yourself.

If the user sends only a screenshot without URL: audit what's visible, but explicitly note that you can only see what's in the image.

Extract:
- Product name, price, variants
- Gallery composition (count images, identify if AI-generated vs real)
- Copy blocks (headline, bullets, product description, reviews)
- Trust signals visible
- Payment methods shown
- Shipping information
- Social proof (reviews, stats, UGC)
- Sections present and sections missing

### Step 2: Classify the store type

Before scoring, classify quickly — it changes what "good" looks like:

| Type | Identifying signals | What to prioritize |
|---|---|---|
| **Dropshipping from China** | AI images, 10-16 day shipping, generic product name, generic descriptions | Trust signals, shipping transparency, price justification |
| **Israeli-manufactured / sourced** | Hebrew product names native, real product photos, fast shipping | Brand story, premium positioning, community |
| **Pro brand with budget** | Custom photography, video, polished design, established social proof | Conversion optimization, A/B testing, advanced upsells |
| **Hobbyist / small seller** | Basic theme, minimal copy, few products | Fundamentals first: one great product page, basic trust stack |

**Important**: Always be direct about what you're seeing. If the product looks like generic dropshipping, say so gently but clearly — the user needs to know this to address the credibility gap. Don't be polite and skip it.

### Step 3: Identify the CRITICAL issues first

Before anything else, scan for **deal-breakers** — things that prevent conversion from happening at all. These get called out at the top of the audit, before any improvement suggestions.

**Common critical issues:**

1. **"אזל במלאי" / Out of stock** — No sale can happen. Top priority.
2. **Long shipping times** (>7 days for Israeli customers) — Massive conversion killer in Israel.
3. **No payment methods visible** — Breaks trust.
4. **Broken add-to-cart** — The site doesn't work.
5. **No mobile optimization** — 85% of Israeli traffic is mobile. A desktop-only site loses them.
6. **Contradictions on the page** — "+368 bought this month" above "Out of stock" is one example. These destroy trust.
7. **Missing legal pages** — No return policy, no privacy policy. Illegal in Israel and signals untrustworthy.
8. **Obviously fake reviews** — Stock avatar URLs, fake names like "א. ד.", identical review times. Israelis spot these fast.
9. **Dead links in navigation** — 404s on Terms, Privacy, About.
10. **Auto-playing audio/video with sound** — Causes immediate bounces.

### Step 4: Score section-by-section

Use this scoring rubric. Apply to each section present on the page. For sections that should exist but don't — mark as 0/10 with a brief note.

**Scoring scale:**
- 9-10: Excellent. Top 5% of stores in this category.
- 7-8: Good. Works well, minor tweaks possible.
- 5-6: Average. Functional but not converting at its potential.
- 3-4: Weak. Likely hurting conversion.
- 1-2: Broken or missing critical elements.
- 0: Section doesn't exist when it should.

Reference `product-page-blueprint.md` for the 10 standard sections of a PDP. Reference `homepage-blueprint.md` for the 10 standard sections of a homepage.

### Step 5: Generate concrete rewrites and alternatives

**Never just say "improve the copy" or "the design is weak."** Every weak element gets a concrete proposal.

**Bad audit note:**
> "הכותרת לא טובה מספיק."

**Good audit note:**
> "הכותרת הנוכחית: 'PalmCalm - היד הביונית'
>
> היא בינונית — 'היד הביונית' נשמע מפוברק. הצעות חלופיות:
> - 'הצוואר שלך לא נועד להחזיק מסך 9 שעות ביום.'
> - 'מסאז'ר צוואר שמרגיש כמו ידיים אמיתיות.'
> - '15 דקות. כתפיים משוחררות.'
>
> מומלץ לבדוק A/B בין 1 ל-2."

### Step 6: Prioritize the TOP 3

At the end of the audit, **always** include a "if you only do 3 things" section. Users get overwhelmed by 20-item improvement lists. The top 3 should be:

1. **High impact** (addresses a big conversion blocker)
2. **Achievable in <1 day** (no custom development needed)
3. **Cheap** (uses existing apps or copy-paste code from this skill)

### Step 7: Deliver as a downloadable document

Audit reports are always long. Don't dump them in chat. Create a markdown file, save to `/mnt/user-data/outputs/`, and use `present_files` to give the user a downloadable copy.

Keep the in-chat message short:
- Brief sentence confirming the audit is done
- The 3 critical issues (in 2-3 bullets max)
- The top 3 improvements (in 2-3 bullets max)
- "הדו"ח המלא בקובץ למעלה ↑"

---

## Audit report template

```markdown
# ביקורת דף מוצר — [שם המוצר]
### [שם החנות] | [קטגוריית מוצר]

---

## סקירה מהירה

**זוהה מהאתר:** [תיאור המוצר, המותג, קהל היעד המשוער]

**סוג חנות:** [דרופשיפינג / ייצור ישראלי / מותג עם תקציב / חנות קטנה]

**כיוון מותג משוער:** [א' - ה' לפי הסקיל הראשי]

---

## 🚨 בעיות קריטיות לטיפול מיידי

[רק אם יש כאלה. אם אין — לדלג על הסקשן הזה.]

### 1. [הבעיה]
[הסבר קצר + פעולה מיידית]

### 2. [הבעיה]
[...]

---

## 📋 ביקורת סעיף-אחר-סעיף

### SECTION 1: [שם] — ציון X/10

**מה עובד:**
- ✅ [...]

**מה לשפר:**
- ❌ [...]
- ⚠️ [...]

**המלצה מעשית:**
[הצעה קונקרטית עם קופי/קוד מוכן להחלפה]

[חזור על זה לכל סקשן]

---

## 🎯 3 ההמלצות הכי חזקות

### 1. [שם ההמלצה]
- **פעולה:** [בדיוק מה לעשות]
- **השפעה:** [צפי שיפור]
- **זמן:** [כמה זמן לוקח]

### 2. [...]

### 3. [...]

---

## סיכום ניקוד

| סקשן | ציון |
|---|---|
| [...] | X/10 |
| **ממוצע כולל** | **X/10** |

[משפט סיכום על המצב הכללי — האם הבסיס טוב, מה הדרך לדירוג גבוה יותר.]
```

---

## Common patterns to watch for

### Patterns that indicate weak conversion

1. **"Wall of text" syndrome** — Long paragraphs with no visual breaks. Israelis skim; they don't read.
2. **Overly marketing copy** — "הפתרון המושלם!", "חווה את הקסם!", "שנה את חייך!" — these phrases signal low-effort dropshipping.
3. **Missing "why now" urgency** — No reason to buy today vs tomorrow.
4. **Gallery stuffing** — 10-15 images where 5 would convert better. Each image should serve a specific purpose.
5. **Hidden shipping costs** — Buyers find out at checkout, abandon at 60-70% rates.
6. **Single-variant tyranny** — Only one size/color option when users expect choice.

### Patterns that indicate dropshipping (handle with care)

- AI-generated hero images (characteristic smoothness, "plastic" skin, weird hands)
- 10-16 day shipping times
- Product named with English keywords translated literally ("Dual-Use Professional Cervical Massager")
- Generic product descriptions with "amazing features" lists
- Reviews with "uifaces" or stock avatar URLs
- All images showing the same person in different poses (usually an AI subject)

**When you identify dropshipping:** Don't judge the user — many successful Israeli stores are dropshipping businesses. Help them optimize within that reality:
- Build trust through transparent shipping ("נשלח ישירות מהמפעל — 10-14 ימים, וזו הסיבה שהמחיר 50% מתחת למתחרים")
- Invest in Israeli customer service (WhatsApp, Hebrew email, real phone)
- Collect real reviews from real customers
- Use their own photography for at least the hero image

### Patterns that indicate the site has potential

- Good product-market fit signals (relevant reviews, specific use cases mentioned)
- Original photography even if minimal
- Clear category positioning
- Working checkout flow
- Responsive mobile design

When these are present, the audit becomes more about optimization (the 3rd-order improvements) rather than foundational fixes.

---

## When the user disagrees with the audit

The user may push back: "but my reviews ARE real," "my shipping time is fine," "the copy is great." Handle this calmly:

1. **Don't backpedal out of politeness.** If the critique is valid, it's still valid. Soften tone, not substance.
2. **Ask for evidence.** "אם הביקורות אמיתיות, אשמח לראות 2-3 דוגמאות של לקוחות אמיתיים שמסכימים לחלוק שם מלא ותמונה. אם יש כאלה — מעולה, נחליף את האווטרים הנוכחיים בתמונות שלהם."
3. **Offer a test, not an argument.** "בוא ננסה A/B — שבוע עם הקופי הישן, שבוע עם החדש. המספרים יחליטו."

---

## Things to never do in an audit

- **Never** criticize without offering an alternative. "זה רע" בלי "תחליף ל-X" הוא חסר ערך.
- **Never** recommend a complete redesign as the first step. Always prioritize the 3-5 changes with highest impact-to-effort ratio.
- **Never** pretend a bad site is good to avoid hurting feelings. The user came for feedback; give it honestly.
- **Never** use technical jargon without explanation. "CLS", "LCP", "Core Web Vitals" — either explain or translate.
- **Never** make up statistics. If you don't know the exact number, say "צפי שיפור של 5-15%" not "צפי שיפור של 12.3%".
