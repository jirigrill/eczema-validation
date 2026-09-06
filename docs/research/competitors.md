# Competitor teardown: eczema and food-trigger tracking apps

Research ticket: [#3](https://github.com/jirigrill/eczema-validation/issues/3). Map: [#1](https://github.com/jirigrill/eczema-validation/issues/1).

Data collected **2026-09-05**, US storefront unless stated.

## Verdict first

**(c) genuinely thin on the eczema side — but thin because nobody has made money there, not because nobody has tried.**

The precise read, in four parts:

1. **Eczema-specific tracking is a graveyard, not a market.** The single largest eczema tracker in the US — [EczemaWise](https://apps.apple.com/us/app/eczemawise-eczema-skin-care/id1522743215), built by the National Eczema Association — is **shutting down**. Its own App Store listing opens: *"\*\*New account creation has ended. Existing users may continue using the app through December 18, 2026.\*\*"* It had **217 iOS ratings** and **5K+ Play installs** after six years, free, with a national patient charity's mailing list behind it. [Leo Pharma's "Imagine"](#imagine-leo-pharma) was withdrawn from both stores in 2022. Every remaining eczema app with any ratings at all is in the **double digits**.
2. **A 2026 wave of near-identical indie subscription clones is already here, and all of them have zero traction.** At least six eczema trackers launched or shipped in 2026 charging $6.99/mo — including two (`EczemaTrack: Baby Rash Tracker`, `Baby W/O Allergies`) that are *the exact product this map proposes*, down to the maternal elimination diet. All have **0 ratings**. Idea-level differentiation is gone; execution and distribution are the whole game.
3. **The willingness to pay is real, but it lives one aisle over, in baby food-introduction.** [Solid Starts](https://apps.apple.com/us/app/solid-starts-baby-first-foods/id1564189151) has **44,363 iOS ratings + 1M+ Play installs** and charges roughly **$100/year** — and its low-star reviews are wall-to-wall complaints about a *broken food/reaction tracker*. That is the only demonstrated paying parent audience in this sweep.
4. **The standing caveat in [#1](https://github.com/jirigrill/eczema-validation/issues/1) survives this research intact and is arguably strengthened.** Nothing here shows an under-served demand that a better app captures. It shows a category where good, well-funded, well-distributed attempts died. Distribution is the failure mode, and this research found no evidence against that.

Detail, tables and the ranked complaint list follow.

---

## Method and limits

- **Apple metadata** (price, rating, rating count, current-version release date, description) comes from Apple's own iTunes lookup/search API — first-party and reproducible:
  `curl -s "https://itunes.apple.com/lookup?id=<id>&country=us"`, `curl -s "https://itunes.apple.com/search?term=<q>&country=us&entity=software&limit=30"`.
- **Apple review quotes** come from Apple's own customer-review RSS feed:
  `curl -s "https://itunes.apple.com/us/rss/customerreviews/id=<id>/sortBy=mostHelpful|mostRecent/page=<n>/json"`, filtered to `im:rating <= 3`. All quotes below are verbatim from that feed.
- **Google Play** figures come from the live listing pages.

**Three limits, stated rather than papered over:**

1. **Apple does not expose in-app-purchase prices through the iTunes API**, and the storefront HTML is client-rendered and rate-limited. Where an Apple subscription price appears below, it is either **stated in the app's own store description** (cited as such) or **stated by a reviewer** (cited as such). No Apple IAP price here is inferred.
2. **The Apple review RSS feed is sparse and rate-limited.** It returned nothing for several apps (EczemaWise low-star reviews via `mostRecent`, Nia, ATOPIYO, Solid Starts on some passes). Absence of quotes below means the feed returned none, **not** that no such reviews exist.
3. Some Google Play sidebar stats (star counts, install buckets) did not render for a few listings; those are marked *not verified* rather than estimated.

---

## Group 1 — Eczema-specific trackers

### 1a. The ones with any measurable users

| App | Developer | Store | Price | Ratings / installs | Last update | Audience |
|---|---|---|---|---|---|---|
| **EczemaWise** — *sunsetting 2026-12-18* | National Eczema Association | [iOS](https://apps.apple.com/us/app/eczemawise-eczema-skin-care/id1522743215) · [Play](https://play.google.com/store/apps/details?id=com.eczemawiseapp) | Free, no IAP | iOS 4.64 / **217**; Play 4.1 / 57, **5K+ installs** | 2026-04-29 (iOS); Apr 28 2026 (Play) | Adult sufferers. **US only** — not available on the GB storefront. |
| **EczemaLess, an AI Eczema Guide** | Polyfins Technology Inc | [iOS](https://apps.apple.com/us/app/eczemaless-an-ai-eczema-guide/id1464477139) · [Play](https://play.google.com/store/apps/details?id=eczemaless.ai.tibot) | Free, no IAP on Play listing | iOS US 4.60 / **65**; iOS GB 3.8 / 10; iOS DE 1.33 / 3; Play 4.2 / 165, **10K+ installs** | **2024-12-23** (iOS — stale); Dec 28 2025 (Play) | Adults. Self-classified as *Clinical Decision Support* "NOT intended to be used by Patients for self diagnosis or self treatment." |
| **Eczema App Nia** | Nia Health GmbH (Charité spin-off) | [iOS](https://apps.apple.com/us/app/eczema-app-nia/id1493690952) · [Play](https://play.google.com/store/apps/details?id=de.niahealth.niaapp) | Free + Premium (price shown only after signup, see complaint #6). **Reimbursed by German health insurers.** | iOS US 5 / 3; **iOS DE 4.52 / 136**; iOS GB 5 / 1; Play 4.5 / 238, **50K+ installs** | 2026-08-14 | Both — description says "their own health (or their affected child's)". **German market; effectively absent from US/UK.** |
| **Eczema Tracker** | Redblink Inc | [iOS](https://apps.apple.com/us/app/eczema-tracker/id1080899152) | Free | 3.61 / **18** | **2021-07-23** — abandoned | Both ("From one parent to another, from one eczema patient to another"). Logs food allergy + pollen/weather. |
| **Eczema CARE+** | Pierre Fabre Eczema Foundation | [iOS](https://apps.apple.com/us/app/eczema-care/id1635967417) · [Play](https://play.google.com/store/apps/details?id=com.eczemafoundation.eczemacareplus) | Free, no IAP | iOS **0 ratings**; Play **10K+ installs** | 2026-04-22 | Adults. PO-SCORAD + AI photo severity. No diet logging. |
| **My Eczema Tracker** | The University of Nottingham | [iOS](https://apps.apple.com/us/app/my-eczema-tracker/id1625064227) · [Play](https://play.google.com/store/apps/details?id=my.eczema.tracker) | Free | iOS US **0**; iOS GB 4 / 1 | 2026-08-10 | **Explicitly parents**: "track your or your child's eczema weekly". POEM + RECAP questionnaires only — no photos, no food. Academic, not a product. |
| **Visual Eczema Care — ATOPIYO** | ATOPIYO LLC | [iOS](https://apps.apple.com/us/app/visual-eczema-care-atopiyo/id6475762535) | "Free to use, anonymous, and ad-free" (own description) | 5 / **6** (US) | 2025-09-23 | Adults. **Community-first** (60,000+ posts), Japan-origin. The only one whose moat is social, not analytical. |
| **Living with Eczema** | M3 (EU) Limited | [Play](https://play.google.com/store/apps/details?id=co.uk.m3europe.ohc.eczema) | Free | **100+ installs** | Feb 10 2026 | "patients and their parents or carers". Photo journal only. |
| **Eczema Tracker – Skin Diary** | Clarity Digital Therapeutics Inc | [iOS](https://apps.apple.com/us/app/eczema-tracker/id6745561801) · [Play](https://play.google.com/store/apps/details?id=eczema.tracker.psoriasis.skin.rash.diary) | Play shows IAP; tiers not verified | iOS **0 ratings**; Play **1K+ installs** | 2026-03-09 (iOS) | Adults ("designed for adults"). SCORAD/EASI + PDF/CSV export. |

<a id="imagine-leo-pharma"></a>**Imagine (Leo Pharma) — dead.** `https://play.google.com/store/apps/details?id=com.leo_pharma.imagine` returns **HTTP 404**; the listing is gone. Pharma withdrew it around July 2022. A pharmaceutical company with a dermatology franchise could not sustain an eczema tracker.

### 1b. The 2026 clone wave — every one of them at 0–3 ratings

All free to download, all subscription-gated, all iOS.

| App | Developer | Store | Stated price | Ratings | Last update | Note |
|---|---|---|---|---|---|---|
| **EczemaTrack: Baby Rash Tracker** | Jorge Hernandez | [iOS](https://apps.apple.com/us/app/eczematrack-baby-rash-tracker/id6787539172) | **"$6.99/month or $39.99/year"**, 7-day trial (own description) | **0** (US, GB, DE) | 2026-09-02 | **This is our product.** 15-region body map front/back, per-area severity, allergen logging, 24–72h lagged correlation, PDF/CSV, on-device only, no account. Launched 2026-07-09. |
| **Itchwise: Eczema & Skin Diary** | Qingdao Ketai Software Co.,Ltd. | [iOS](https://apps.apple.com/us/app/itchwise-eczema-skin-diary/id6789539584) | **"Itchwise Pro: $6.99/month or $39.99/year. Lifetime $99.99."** (own description) | **0** | 2026-07-20 | Identical price point to EczemaTrack. |
| **Baby Eczema Tracker & AD Diary** | 骋飞 武 | [iOS](https://apps.apple.com/us/app/baby-eczema-tracker-ad-diary/id6775365272) | Free download; IAP not verified | **0** | 2026-07-22 | Parent-targeted, opens on the same 3am scene our positioning would. |
| **Eczemate: Eczema Skin Care** | Foresight Computing, Inc. | [iOS](https://apps.apple.com/us/app/eczemate-eczema-skin-care/id6759606605) | Hard paywall: "an active Eczemate Pro subscription is required to unlock the trackers, scanners, insights" (own description); $ not stated | 4.33 / **3** | 2026-06-16 | "Whether you're caring for your child or managing your own skin". |
| **EczemaEase: Eczema Tracker** | Deniz Demirel | [iOS](https://apps.apple.com/us/app/eczemaease-eczema-tracker/id6766025259) | Premium sub, 3-day trial; $ not stated | **0** | 2026-05-13 | **Multi-child**: "Manage eczema for multiple family members -- including children -- from one account." |
| **Aureya: Eczema & Skin Tracker** | MOLABS LLC | [iOS](https://apps.apple.com/us/app/aureya-eczema-skin-tracker/id6757940854) | Premium, 7-day trial; $ not stated | 5 / **1** | 2026-04-23 | "food-skin insights" is a Premium feature. |
| **Bloomly: Eczema Skin Tracker** | Adrian Neil Dimaculangan | [iOS](https://apps.apple.com/us/app/bloomly-eczema-skin-tracker/id6773816024) | "Bloomly Pro... Monthly or annual" (own description) | **0** | 2026-08-06 | |
| **Alara — AI Eczema Tracker** | Dylon Tan | [iOS](https://apps.apple.com/us/app/alara-ai-eczema-tracker/id6755063841) | Subscription; $ not stated | 3 / **1** | 2025-12-10 | |
| **SkinFam: Skin Eczema Diary** | malin haga idsøe | [iOS](https://apps.apple.com/us/app/skinfam-skin-eczema-diary/id6786998215) | Not stated | **0** | 2026-08-25 | |
| **Eczema Tracker - FlareLog** | kurihara kazuki | [iOS](https://apps.apple.com/us/app/eczema-tracker-flarelog/id6757834180) | Not stated | **0** | 2026-07-22 | |
| **clara health: treat eczema** | Go Terminal Limited | [iOS](https://apps.apple.com/us/app/clara-health-treat-eczema/id6745744870) | Not stated | 5 / **2** | 2025-08-18 | |
| **Atopic App – AI Eczema Manager** | Iqutis Labs Ltd | [iOS](https://apps.apple.com/us/app/atopic-app-ai-eczema-manager/id1593177147) · [Play](https://play.google.com/store/apps/details?id=com.atopicapp) | Not verified | **0** (iOS) | 2026-04-07 | |

**Read this block carefully before any go decision.** Twelve apps, at least eight of them shipped in the last twelve months, all converging on the same $6.99/mo shape, and their *combined* iOS rating count is under twenty. Either the category cannot be reached with an indie marketing budget, or these builders are all worse at distribution than we would be. The base rate does not favour the second reading.

---

## Group 2 — Baby food-introduction and infant allergy trackers

### 2a. The direct-hit competitors (maternal diet → infant reaction)

| App | Developer | Store | Price | Ratings / installs | Last update | Note |
|---|---|---|---|---|---|---|
| **Baby W/O Allergies** | Jirina Brazdova (babyapp.cz) | [iOS](https://apps.apple.com/us/app/baby-without-allergies/id6776690582) · [Play](https://play.google.com/store/apps/details?id=cz.babyapp.app) | Free + IAP; tier not verified | iOS **0**; Play **100+ installs** | 2026-08-31 | **The exact product.** Own listing: "a guided elimination diet, safe step-by-step allergen testing, and a daily symptom diary built specifically for infants with suspected food allergies, CMPA or atopic eczema." Tracks eczema flare severity *and location*, symptom photos, and explicitly serves "Breastfeeding mothers following a maternal elimination diet." |
| **Baby Allergy Tracker: AllerLog** | Arai Tech L.L.C-FZ | [iOS](https://apps.apple.com/us/app/baby-allergy-tracker-allerlog/id6775501131) | Free | **0** | 2026-08-20 | Meals + mood/sleep/stool per ingredient, AI pattern flagging. No skin regions/photos. |
| **AllergyLog: Food Allergies** | Anh Phong | [iOS](https://apps.apple.com/us/app/allergylog-food-allergies/id6760707963) | Free | **0** | 2026-03-23 | Top-9 allergen introduction, reaction log with photos, PDF/CSV. |
| **Baby Food & Allergy Tracker** | Athleticus Inc. | [iOS](https://apps.apple.com/us/app/baby-food-allergy-tracker/id6736767112) | **$1.99 one-time** — the only paid-upfront app in the sweep | 5 / **1** | 2026-08-15 | "no account, no sign-up, no cloud... pay once, use forever." Multi-child. No photos, no body regions. |
| **Food Allergy Tracker – Lergy** | Karol Jaworski | [iOS](https://apps.apple.com/us/app/food-allergy-tracker-lergy/id6760373418) | Free | 4.5 / **2** | 2026-07-13 | Photos, symptom body-location tagging, correlation engine, PDF report. Not baby-specific. |

### 2b. The one that proves parents pay

| App | Developer | Store | Price | Ratings / installs | Last update | Audience |
|---|---|---|---|---|---|---|
| **Solid Starts: Baby First Foods** | SolidStarts LLC | [iOS](https://apps.apple.com/us/app/solid-starts-baby-first-foods/id1564189151) · [Play](https://play.google.com/store/apps/details?id=com.digitas.solidstarts) | Free database + "All Access monthly or yearly plan" (own description; no $ in listing). **Reviewers state $100/year** — see complaint #1 | iOS **4.90 / 44,363**; Play **4.86 / 24,518, 1M+ installs** | 2026-08-31 | Parents, 6–18mo. Content-first (400+ food database, choking/allergen guidance), tracker bolted on. |
| **Baby Food Tracker & BLW: Avo** | Erhan Kiroglu | [iOS](https://apps.apple.com/us/app/baby-food-tracker-blw-avo/id6474271729) · [Play](https://play.google.com/store/apps/details?id=com.linasoft.startsolids) | Free + IAP | iOS 4.9 / 11; Play **4.57 / 526, 10K+** | 2026-08-31 | Parents. Marks foods liked/disliked/allergic. |
| **BLW Meals: Starting Solids** | BLW SOCIAL PTE. LTD. | [iOS](https://apps.apple.com/us/app/blw-meals-starting-solids/id1540196240) · [Play](https://play.google.com/store/apps/details?id=com.n51951dd8177.app) | Free + IAP | iOS 4.66 / 317; Play **3.43 / 417, 100K+** | 2026-09-02 | Parents. Recipes, not reactions. |
| **Spokin – Manage Food Allergies** | Spokin, Inc. | [iOS](https://apps.apple.com/us/app/spokin-manage-food-allergies/id1201909035) | Free | 4.63 / **902** | 2026-07-23 | Families with diagnosed allergies. Restaurant/product safety + community. Not a symptom diary. |

### 2c. General baby loggers a parent already has installed

None of these publicise photo-based per-region skin tracking or maternal diet logging; food is a generic meal note. They matter because **they own the parent's daily-logging habit already**.

| App | iOS rating / n | Play rating / n · installs | Last update |
|---|---|---|---|
| [Baby Tracker - Newborn Log](https://apps.apple.com/us/app/baby-tracker-newborn-log/id779656557) (Nighp) | 4.80 / **227,267** | 4.91 / 71,046 · [1M+](https://play.google.com/store/apps/details?id=com.nighp.babytracker_android) | 2026-09-04 |
| [Huckleberry: Baby Tracker](https://apps.apple.com/us/app/huckleberry-baby-tracker/id1169136078) | 4.92 / **72,699** | 4.91 / 35,888 · [1M+](https://play.google.com/store/apps/details?id=com.huckleberry_labs.app) | 2026-09-04 |
| [Baby Tracker & Newborn Log](https://apps.apple.com/us/app/baby-tracker-newborn-log/id551448817) (Med ART) | 4.78 / **31,488** | — | 2026-08-28 |
| [Nara Baby & Pregnancy Tracker](https://apps.apple.com/us/app/nara-baby-pregnancy-tracker/id1444639029) | 4.94 / 23,372 | 4.89 / 6,791 · [100K+](https://play.google.com/store/apps/details?id=com.naraorganics.nara) | 2026-06-13 |
| [Glow Baby](https://apps.apple.com/us/app/glow-baby-tracker-growth-app/id1077177456) | 4.67 / 23,456 | not verified | 2025-11-05 |
| [Ovia Parenting](https://apps.apple.com/us/app/ovia-parenting-baby-tracker/id1106614359) | 4.77 / 10,197 | 4.56 / 13,090 · [500K+](https://play.google.com/store/apps/details?id=com.ovuline.parenting) | 2026-05-04 |

Note the scale gap: **Baby Tracker has 227,267 iOS ratings; every eczema app on earth combined has fewer than 400.** That is the shape of the category, not a rounding error.

*Not apps:* **Ready. Set. Food!** and **Lil Mixins** are physical allergen mix-in products with no store presence found.

---

## Group 3 — General symptom / elimination-diet trackers

| App | Developer | Store | Price | Ratings / installs | Last update | Audience |
|---|---|---|---|---|---|---|
| **mySymptoms Food Diary** | SkyGazer Labs Ltd | [iOS](https://apps.apple.com/us/app/mysymptoms-food-diary/id405231632) · [Play](https://play.google.com/store/apps/details?id=com.sglabs.mysymptoms) | Free + subscription, 7-day trial. **The developer's own FAQ declines to publish a price**, saying it varies by country and is shown only at the in-app paywall. Older reviews reference a $2.99–$3 one-off. | iOS **4.60 / 4,040**; Play **3.95 / 3,543, 100K+ installs** | 2026-08-20 (iOS); Apr 16 2026 (Play) | Adults. **Its own listing names eczema** as a tracked condition — a direct substitute. "Family access" = multi-device for one person, **not** multi-person. No photos. |
| **Bearable — Symptom Tracker** | Bearable Ltd | [iOS](https://apps.apple.com/us/app/bearable-symptom-tracker/id1482581097) | **$6.99/mo or $34.99/yr** (bearable.app pricing page), often discounted to $18.99/yr; 7-day trial | iOS **4.77 / 6,234**; Play 4.6 / 10.3K, 500K+ | 2026-08-05 | Adults, chronic illness. No child/dependent mode. No photos. |
| **Cara Care: IBS, FODMAP** | HiDoc Technologies GmbH | [iOS](https://apps.apple.com/us/app/cara-care-ibs-fodmap-tracker/id1133687886) | Free + paid 12-week programme; $ not verified | iOS 4.78 / 4,650; Play 4.1 / ~2.5K, 100K+ | **2020-10-27** (iOS — stale) | Adults, GI. |
| **Guava: Health Tracker** | Guava Health, Inc. | [iOS](https://apps.apple.com/us/app/guava-health-tracker/id1622255863) | Free; Premium **$8/mo or $78/yr** (guavahealth.com/plans). A discounted **Family Plan** exists, price not shown. | iOS 4.81 / 892; Play 4.41 / ~1.7K, 130K+ | 2026-08-18 | Adults, complex/undiagnosed conditions. |
| **Migraine Buddy** | Voluntis | [iOS](https://apps.apple.com/us/app/migraine-buddy-track-headache/id975074413) · [Play](https://play.google.com/store/apps/details?id=com.healint.migraineapp) | Free core; **MBPlus from $9.99/mo** | iOS **4.80 / 41,586**; Play 4.83 / ~64K, 1M+ | 2026-08-24 | Adults. **The pricing archetype**: free logging, paid prediction. Proof a single-condition trigger diary can reach scale — in a condition with ~10× the adult prevalence and no 18-month churn. |
| **Monash FODMAP Diet** | Monash University | [iOS](https://apps.apple.com/us/app/monash-fodmap-diet/id586149216) | **$7.99 one-time** — the only non-subscription of note | iOS 4.22 / 2,568; Play 4.31 / ~4.5K | 2026-03-12 | Adults, IBS. |
| **Bowelle – The IBS tracker** | Bowelle AB | [iOS](https://apps.apple.com/us/app/bowelle-the-ibs-tracker/id1436064640) | Free; IAP not verified | 4.74 / 2,238 | 2026-08-27 | Adults, GI. |
| **Talli Health & Symptom Tracker** | BabyLogger, LLC | [iOS](https://apps.apple.com/us/app/talli-health-symptom-tracker/id1505549920) · Play `me.talli.symptomtracker` | Free base; add-ons "as low as $1.99/month" (talli.me) | 4.52 / **46** | **2023-10-26** — stale | **The only multi-person tracker found.** "Add yourself and any loved ones... give others access to log for individuals on your account" and "Add photos where needed, such as for eye or skin inflammation or rashes." Generic, not eczema-shaped. 46 ratings. |
| **Trigger: Skin Tracker** | Surya Palsam | [iOS](https://apps.apple.com/us/app/trigger-skin-tracker/id6787020115) | Not verified | **0** | new | Structurally the closest: "Add weekly photos and get an AI skin-score estimate... per-zone AI estimates... see possible triggers ranked." Framed for adult skincare/shaving, not infants. |
| **Fig: Food Scanner & Guide** | Food is Good, Inc. | [iOS](https://apps.apple.com/us/app/fig-food-scanner-guide/id1564434726) | Free | 4.71 / 16,131 | 2026-09-02 | Safe-food shopping, not a diary. |
| **Spoonful: Diet & Food Scanner** | Spoonful Inc. | [iOS](https://apps.apple.com/us/app/spoonful-diet-food-scanner/id1481914232) | Free | 4.62 / 1,818 | 2026-08-28 | Scanner, not a diary. |

**Flaredown** did not appear in any current iTunes search; its live store presence in 2026 is *not verified* — treat as likely delisted.

---

## Ranked review complaints — the gap list

Ranked by how often the theme recurred **and** how directly it bears on our product shape. All quotes verbatim from Apple's customer-review RSS feed; ratings and reviewer handles as returned by the feed.

### 1. Subscription price resented, especially against a short use window — the single loudest theme

This is the biggest constraint on the commercial thesis. Parents say out loud that the *duration of need* does not justify a recurring price.

> **1★, KC448** (Solid Starts): "This app makes you create an account and profile for you and your baby, makes you answer a lot of questions, promises a lot of stuff, and then tells you that you have to pay a monthly or yearly subscription to use pretty much anything on the app. For one, this is ridiculous because **you're only going to use this app for a few months or maybe a year at most** and then your baby will be eating regular food exactly how you make it anyway so this app will be useless then so obviously they're just trying to get you to forget you have the subscription so they can keep taking your money"

> **3★, 96Nikki96!** (Solid Starts): "The premium subscription cost $10 last year around this time. **Now it is $100.** That is an insane price increase... **Most parents are using this app for maybe 6 months consistently.** You could potentially make more of a profit by charging less bc more parents would be willing to"

> **3★, H_G\_** (Solid Starts): "I don't recommend buying the subscription. It's **literally $100 for information that I could easily find by googling**, asking my pediatrician, or buying an $8 baby-led weaning book."

> **2★, Ninjafoot2** (Solid Starts): "a GIANT portion of it is hidden by pay walls and **I'm not paying $20 a month** for an app as IMO that's pretty expensive."

> **3★, Sarahdenali** (Solid Starts): "Would've have much rather **paid for the months we used the app** and had the option to opt-out and cancel the subscription— but since there was only one annual s[ubscription]..."

> **1★, Benjamin Michaelis** (Nia, Google Play, Aug 29 2023): "Very good concept but **the extremely high price to enable identification of triggers is only shown after account creation.**"

> **3★, emiru19** (mySymptoms): "The app never asked for my card info or for an upgrade to premium or warned me about a trial period that I would be charged after. I found a charge to my apple account about a week after downloading... **sneaky charge**."

**Bearing on us.** This maps directly onto the map's own churn caveat in [#1](https://github.com/jirigrill/eczema-validation/issues/1). The ICP has an intrinsically short window and *knows it*. A monthly subscription is the pricing model the market is angriest about; a modest lifetime unlock is what several reviewers explicitly ask for — and lifetime unlock cannot hit $3–5k/mo without ~1,000 new buyers **per month**, not 1,000 total. That arithmetic deserves to be run before the landing page is written.

### 2. The correlation/insight engine is the paid feature, and it does not convince

Every app in this sweep paywalls "insights". Every reviewable one is accused of insights being wrong, opaque or trivial. This is the feature our product's entire premise rests on.

> **2★, tpaul1987** (mySymptoms): "I was drinking a protein shake every morning with 3 or so ingredients in it and like clockwork, I'd have an upset stomach 30 minutes later. Obviously, it was something in my protein shake, yet **the app missed it** or claims those ingredients had a low chance of being the culprit. Aside from that, it claims 'fruit' is my number one culprit for every single symptom that's logged with 'high confidence' but **I've never logged 'fruit.'**"

> **3★, sweetnsour1826** (Bearable): "**their correlations grid does not give correlation values**, and while that probably doesn't bother most people, **the results and conclusions can be misleading**."

> **3★, River 555** (Bearable): "**The results are not accurate or trustworthy**... there are too many glitches that make me not trust the results. I have spent a lot of time these past few days inputting all my foods and symptoms."

> **3★, EFJ42** (Bearable): "It seems to only be helpful if you track things perfectly, which I don't know if anybody can do. I'll find that I accidentally overlook one thing one day and then suddenly it's **made a correlation that makes no sense. Like it thinks I feel better when I am really stressed**"

> **3★, PacRya** (Bearable): "**The correlations I got mostly confirmed things I already suspected**, and over time the effort of recording symptoms every day started to feel like more hassle than it was worth."

> **3★, just senditomg** (EczemaLess): "I really do not see the use of this app yet. **I log all my information in and you put it on a chart** 🤷🏽‍♀️ I have no use for that."

> **2★, Spammy808** (Eczema Tracker): "The app's benefits **didn't justify the amount of work put into entering everything**."

**Bearing on us.** The wedge is *not* "nobody has a correlation engine". Everybody has one and nobody trusts it. Winning here means being demonstrably right and demonstrably honest about uncertainty — which is a hard, unglamorous, evidence-heavy problem, not a UI problem.

### 3. Logging is too tedious to sustain — the churn mechanism

> **2★, Dragonfreckles** (Bearable, 2-year user): "**This app causes me more anxiety just to use it.** It requires me to fill out dozens and dozens of symptoms at different ratings twice a day. That would be perfectly OK if I felt that I was getting good or even average interpreted information"

> **3★, Apostate_Mage** (Bearable): "a large amount of the symptoms I face are related to food... **manually entering each ingredient is too time consuming to realistically do every meal**."

> **1★, jorjonzn** (mySymptoms): "It is very easy to lose what you have entered if you do not answer the series of prompts correctly, or if you miss a prompt. **It just takes too long to jot something down.**"

> **2★, Salmon Suzy** (mySymptoms): "Too many entries - same meds every day... **should have button 'same as yesterday'**"

> **2★, Skaddict** (Solid Starts): "**every step you need to take is made tedious**... The tracker seemed useful so it tried to add yesterdays food. Looks like I can't add it from the tracker. Off to the food search I go. I then have to answer 3 slides of questions to final[ly]..."

**Bearing on us.** "Two minutes a day" is the promise every one of these apps made and broke. A Copy Meal affordance and a one-tap repeat are not nice-to-haves; they are the retention mechanism.

### 4. The food database is the make-or-break, and everyone's is bad

> **2★, Robin Lamb** (mySymptoms): "**I'm trying to determine if my daughter has a soy allergy. Guess what ingredient this app doesn't allow you to add. Soy!** I tried scanning the barcode for three different common items... None were listed in the database. Forgivable, except that I can't even enter the ingredients in the database because it won't even let me add soy as an ingredient. Waste of money. I'd like a refund."

> **2★, LoúcaSun** (Solid Starts): "today when again I couldn't find a basic food in their database I felt forced to write this review! This app **charges 100!!! $ a year and doesn't have a database of many many foods**, forcing me to google most of the foods I feed my daughter anyways"

> **3★, bitwiseshiftleft** (mySymptoms): "There is one major downside to the user-generated database: **it has many different copies of the same food**, which are included as ingredients in other foods as well."

> **3★, IdeaMan98** (mySymptoms): "**As the inventory is uncontrolled, you end up with 20 versions of everything.**"

> **2★, Shzeller** (mySymptoms): "it doesn't allow you to add ingredients and since it is **missing even common ingredients such as green onions** (not listed under scallions either)"

> **1★, Disappointing for a paid app** (Solid Starts): "**You also can't add foods your baby has tried unless they already exist in the app**, which makes it feel very limited and not truly customizable."

**Bearing on us.** This is genuine validation for the eczema-ios decision to hand-author a curated, cited English catalog with stable slugs rather than crowdsource or scrape one — the two failure modes reviewers describe (missing common foods; twenty duplicate entries of the same food) are exactly the two a curated catalog avoids. But it also validates the *risk*: a curated catalog that is missing "green onions" earns a 2★ review. Free-text fallback is not optional.

### 5. Data loss, sync failure and account walls — the trust killers

> **1★, Heushonnny** (Solid Starts): "**they don't address the fact that we lost all our progress**, that is just gone with this 'upgrade.'... **Do not waste money on this app if you're expecting to rely on it** to help ease your baby into solids because the developer will just pull the rug on you at any time."

> **3★, mt12989** (Solid Starts): "**yesterday it showed that she has tried 15 foods and today it says 0, everything I had logged has disappeared.** I tried to re-add some of the food and now it won't save at all"

> **3★, sadiekinzzz** (mySymptoms): "I have this app on 2 devices but **the information doesn't transfer from one to the other**... All of my other FREE apps work and communicate with each other"

> **1★, SandiH46** (EczemaWise): "I installed this app and **it won't let me log in. Keeps telling me I need to verify my email which I've done 10 times.** Don't waste your time!"

> **1★, tyoesm** (EczemaWise): "- verify email flow didn't work - reset password didn't work - **couldn't try the app**"

> **1★, An0ny m0use** (EczemaWise): "I've tried many times to get signed up, and then it wouldn't connect to send my information. **So I never made it into the app to the features.**"

> **2★, Spammy808** (Eczema Tracker): "I don't like that I could not log out, delete my account, or even see my account through the app. **Seems like the acct creation is just a way to get my email address.**"

> **1★, A0232002** (Eczema Tracker): "After I take my photo to document a flare, **it doesn't save and sends me back to Record empty state.**"

**Bearing on us.** Three of the top-five EczemaWise complaints are *account signup failures* — people who never reached the product. A no-account, CloudKit-private, device-local design sidesteps this entire complaint class outright. It is the cleanest positive signal in this document for the architecture already chosen in `eczema-ios`. Conversely, CloudKit sync failing silently would land us straight in the same bucket.

### 6. Photos and per-region skin detail are missing or too coarse — and parents are the ones asking

> **1★, pass and delete** (EczemaLess): "**I was planning to use this to track my little one's eczema** but quickly decided to delete this app. Zero suggestions for improving gut health which is the primary issue for eczema. **The analysis wouldn't pick up her rashes in photos and doesn't allow for smaller regions to be analyzed (I.e. neck, ankles, back of knees).** Will be looking for another more thorough, detail-oriented, **children-safe and friendly option**. Delete."

> **1★, Portte** (EczemaLess): "**You cannot log your eczema severity on your own.** I would like to be able to rate my itchiness, but the app insists on analyzing your skin for you. In my case, my itchiness far outweighs the look of my skin. **The camera picture itself does not pick up my eczema**, so this app is now completely useless to me."

> **3★, pawsnprints20 in seattle** (mySymptoms): "**I wish there was a way to add photos**... This is crucial when buying your app for medical assessment & diagnostic purposes."

> **1★, Dev183638** (Eczema Tracker): "**I can't add photos because the option doesn't show up**... it's a disaster... I'd rather just do my own tracking in excel :("

**Bearing on us.** The single most on-point review in this entire sweep is `pass and delete`. It is a parent, tracking an infant, who churned for precisely three reasons: no small body regions (neck, ankles, popliteal fossae), no food/gut angle, and not child-appropriate. That is a three-line product brief. **It is also, near-verbatim, the feature list of `EczemaTrack: Baby Rash Tracker`, shipped two months ago.** The gap was real and someone else has already filled it.

Note also the **anti-AI signal**: two of the four quotes above are complaints that AI photo analysis *replaced* self-report and got it wrong. Manual severity entry is a feature, not a fallback.

### 7. Nobody models "one person's diet → another person's symptom"

Not a review theme — a structural absence, which is why it ranks last but matters most.

- **mySymptoms** "Family access" is multi-device sync for one account, not multi-person logging — confirmed by `Robin Lamb`'s 2★ above, a parent hitting the data-model wall while tracking a daughter.
- **Bearable, Cara Care, Bowelle, Monash** — no dependent mode at all.
- **Talli Health** is the only genuine multi-person tracker found, and it is generic ("log for individuals on your account"), photo-capable but not region-scored, and last updated 2023 with 46 ratings.
- **Guava** has an unpriced "Family Plan" of unverified scope.
- Only **Baby W/O Allergies** (100+ Play installs, 0 iOS ratings) explicitly serves "breastfeeding mothers following a maternal elimination diet."

So the maternal-diet→infant-skin relationship is genuinely unoccupied *at scale*. It is also occupied *in kind*, by an app nobody has heard of. Unoccupied-at-scale in a category where nothing reaches scale is weak evidence of opportunity.

---

## What would change this read

Stated so the next ticket can go looking, rather than leaving the conclusion unfalsifiable:

- **Revenue evidence for any eczema app.** Nothing in this sweep establishes that *any* eczema-specific app earns meaningful revenue. Rating counts are a proxy for installs, not for money. A third-party revenue estimate on `EczemaLess` or `Nia` would sharpen this considerably.
- **Why EczemaWise actually closed.** ~~The NEA's stated reason is usage-based.~~ **Partly closed 2026-09-06, and it softens the graveyard reading — see the correction section below.** NEA has published no stated reason anywhere reachable; what is now established is that the app was free with no IAP, and that NEA's own IRS filing puts it at **25,000 users**, not the 5,000 Android installs quoted above.
- **Whether the 2026 clone wave is spending anything on distribution.** If those twelve apps launched with zero marketing, their zero ratings say nothing about the category and everything about their go-to-market. If any of them ran paid acquisition and still got nothing, that is close to decisive.
- **The Solid Starts adjacency.** Its low-star reviews are a working list of a paying audience's unmet needs, in an app that charges ~$100/year and has a million installs. A reaction/trigger tracker positioned *against Solid Starts' broken tracker*, sold to parents already conditioned to pay at that price point, is a materially different and better-evidenced thesis than "an eczema app". That is worth its own ticket before any go/no-go.

---

## Correction, 2026-09-06: the EczemaWise numbers above understate it by 5x

Added after the ticket closed, because it changes a load-bearing figure rather than adding colour. Everything here was fetched 2026-09-06 and is first-party.

**It was never a paid app.** The iTunes lookup API returns `price: 0.0`, `formattedPrice: "Free"`, and the listing carries no in-app purchases. So EczemaWise is **zero evidence about willingness to pay for eczema tracking** — a point the "graveyard" framing above quietly borrows against.

**It had 25,000 users, not 5,000.** NEA's [Form 990 for FY2024](https://cms.nationaleczema.org/wp-content/uploads/2026/04/2024-National-Eczema-Association-Fed-Form-990.pdf), in the program-accomplishments narrative, states verbatim:

> "The EczemaWise mobile app surpassed 25,000 users and received multiple national awards for patient engagement."

The **5K+ figure quoted above is Google Play installs only** — one platform, and the smaller one. The 217 iOS ratings are a ratings count, not an install count. A charity's own IRS filing is a stronger source than either.

**No reason has been published anywhere reachable.** The sunset notice is identical on both stores and gives none:

> "**New account creation has ended. Existing users may continue using the app through December 18, 2026.**"

Beyond that: `nationaleczema.org/eczema-wise/` 404s and so do four other candidate URLs; NEA's own site search for "eczemawise" returns nothing; the post sitemap contains no matching entry; there is no press-room item and no blog post. The FY2025 990, which would cover the decision, is not filed yet.

**What this does to the read.** A national patient charity retiring a **free**, award-winning app with **25,000 users** and no revenue line is consistent with an operating-cost or grant-cycle decision, and is not by itself a demand verdict. Combined with the finding already recorded above — that three of the top-five 1★ complaints are **signup failures**, from people who never reached the product — the honest version is:

- EczemaWise does **not** demonstrate that eczema tracking has a ceiling of 5,000 users.
- It does **not** demonstrate anything about pricing, because it never had a price.
- It **does** still demonstrate that the largest US eczema charity, with 75K email subscribers and 66K Facebook followers behind it, could not sustain the product — which is a real negative, just a weaker and differently-shaped one than "5K installs after six years."

The four negative findings across the sweep still corroborate each other. This one is now the weakest of them, and should not be cited as the strongest.
