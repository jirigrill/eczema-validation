# Ad channels that will take $100 of eczema-parent targeting (US/UK)

Resolves [eczema-validation#6](https://github.com/jirigrill/eczema-validation/issues/6).

**Scope.** Operational ad-policy only: will a platform accept the targeting, the copy, and the
spend. The wider legal posture of health-data commercialization (GDPR Art. 9, DPIA, App Store
medical-claims review) is **out of scope** by the owner's ruling and is not covered here.

**Question.** Which channel will accept ~$100 to put a pre-launch landing page in front of parents
of eczema-prone babies in the US and UK — and will it accept that targeting at all?

**Headline.** Yes, the test is runnable. No platform lets you target eczema directly; every one of
them treats health as a restricted targeting signal. But **Google Search does not restrict
*keywords*** — only audience products — so a parent who types "baby eczema" can be reached
lawfully and by their own declared intent. That is the channel. The binding risks are not the
health policies at all: they are (a) second-person copy that asserts the reader's baby has eczema,
and (b) a thin pre-launch page failing a destination/landing-page review.

---

## Per-platform table

| Platform | Health-condition targeting? | Legal proxies | Copy restriction on "Does your baby have eczema?" | Min spend | CPC est. (US / UK) | Policy source |
|---|---|---|---|---|---|---|
| **Meta** (FB/IG) | **No.** Health interest/cause segments removed Jan 19 2022 | Demographics → Parents (child age bands), Life Events, broad interests, Advantage+ audience, lookalikes (needs a seed you don't have) | **Explicitly prohibited.** Meta's own example: ❌ "Do you have diabetes?" | None — "If you want to spend $5 a week, you can" | ~$1.00–1.75 / lower (3rd-party) | [Personal Attributes](https://transparency.meta.com/policies/ad-standards/objectionable-content/privacy-violations-personal-attributes/) · [targeting removal](https://developers.facebook.com/blog/post/2021/12/08/updating-metas-detailed-targeting-options/) |
| **Google Search** | **Audiences: no.** Health is a sensitive interest category. **Keywords: yes — not in scope of the restriction** | **Search keyword intent** (`baby eczema`), plus predefined Google audiences ("expressly configured without sensitive user signals") | Prohibited by analogy: "Ads that imply knowledge of a user's personal information". Google's published example is financial, not health | No account minimum found stated; budget "entirely up to you" | $0.50–2.00 informational / £0.30–1.20 | [Restricted targeting](https://support.google.com/adspolicy/answer/143465) · [Health category](https://support.google.com/adspolicy/answer/16701855) · [Data collection and use](https://support.google.com/adspolicy/answer/6020956) |
| **Reddit** | **No.** "Physical and mental health" and "Genetic, biometric, or health data" are prohibited sensitive categories. **Medical & Mental Health communities may not be targeted "under any circumstance"** — so r/Eczema is out | **Subreddit targeting** of *non-medical* parenting communities (r/beyondthebump, r/NewParents), `Parenting` interest (`parenthood_v3`), English-only keyword targeting | **No explicit copy rule.** Nearest: "do not use personal information in your ad". Risky at manual review, not banned on its face | **None published.** Reddit's own tip: "Each ad group should have a daily budget of at least $50" | ~$0.10–1.25 (3rd-party, US-skewed) | [Targeting Guidelines](https://business.reddithelp.com/s/article/Reddit-Advertising-Policy-Targeting-Guidelines) · [Audiences](https://business.reddithelp.com/s/article/reddit-audiences) |
| **TikTok** | **No.** "Individual health statuses or disabilities…" is a protected category under the Anti-Discrimination Ad Policy | Interest categories (incl. Baby, Kids & Maternity), behavior targeting, hashtag/keyword, custom + lookalike (1,000-user floor — unusable pre-launch) | **No equivalent published rule.** TikTok has no Meta-style personal-attributes clause. Still high automated-moderation risk | **$50/day campaign, $20/day ad group** → $100 = 5 days, one market | ~$1.00–1.50 / ~$0.60–1.00 (3rd-party) | [Anti-Discrimination](https://ads.tiktok.com/help/article/tiktok-anti-discrimination-ad-policy?lang=en) · [Budget](https://ads.tiktok.com/help/article/budget) |
| **Pinterest** | **No — and proxies are banned too:** "the targeting of proxies for the sensitive categories above is also not allowed" | Broad parenting/baby interests + *neutral* search keywords only. Actalike needs a seed you don't have; **do not upload iOS-derived lists** | **Effectively prohibited twice over** — the targeting clause plus a content ban on ads that "reference sensitive health or medical conditions". The word "eczema" is likely rejectable on its face | **None published.** CPC bid floor **$0.10 US / £0.07 UK** | ~$0.30–0.83 (3rd-party) | [Advertising Guidelines](https://policy.pinterest.com/en/advertising-guidelines) · [Set your bid](https://help.pinterest.com/en/business/article/set-your-bid) |

---

## Meta (Facebook / Instagram)

### Targeting — health segments are gone

Meta removed health-related detailed targeting on 2022-01-19. Verbatim, from Meta's own developer
blog ([source](https://developers.facebook.com/blog/post/2021/12/08/updating-metas-detailed-targeting-options/)):

> starting January 19, 2022, we will be removing some Detailed Targeting options because they
> relate to topics people may perceive as sensitive, such as targeting options referencing causes,
> organizations, or public figures that relate to health, race or ethnicity, political affiliation,
> religion, or sexual orientation. Examples include:
> Health causes (e.g., "Lung cancer awareness", "World Diabetes Day", "Chemotherapy")

Two later contractions matter for planning
([Updates to detailed targeting](https://www.facebook.com/business/help/458835214668072)):

> We started removing the ability to use detailed targeting exclusions on: March 31, 2025 [Ads Manager]

> We started consolidating some of our detailed targeting interest options by combining relevant
> interests into new groupings on: June 23, 2025 … Existing campaigns created before June 23 can
> continue running and will not be affected until January 15, 2026. At this point they will stop
> delivering if the impacted options have not been removed or replaced.

So: no eczema segment, no exclusions, and an interest taxonomy actively being coarsened. The only
proxy is parental status / life event + broad interest. Meta does not publish its segment taxonomy,
so the exact labels ("Parents (All)", "New parents (0-12 months)") must be **verified in Ads Manager**
rather than cited — they are not in any primary Meta document I could find.

### Copy — this is where Meta is decisive, and it is quotable

[Privacy Violations and Personal Attributes](https://transparency.meta.com/policies/ad-standards/objectionable-content/privacy-violations-personal-attributes/), verbatim:

> Ads must not contain content that shares or asks for private information about users. In addition,
> ads must not contain content that asserts or implies personal attributes. This includes direct or
> indirect assertions or implications about a person's race, ethnicity, religion, beliefs, age,
> sexual orientation or practices, gender identity, disability, **physical or mental health
> (including medical conditions)**, vulnerable financial status, voting status, membership in a
> trade union, criminal record, or name.

> Ads can't:
> - Share or ask for personal attributes of a user or user's family
> - Imply that the advertiser is aware of someone's personal attributes **or the personal attributes
>   of their family**
> - …
> - Imply knowledge of Medical information of a user or user's family

The "or their family" limb is the one that kills the obvious creative: it is not a defence that the
eczema is the *baby's* and not the reader's.

Meta's own worked examples under **PHYSICAL OR MENTAL HEALTH AND DISABILITY**:

> ✅ "Bulimia counseling available"
> ✅ "Depression counseling"
> ✅ "New diabetes treatment available"
> ❌ "Do you have diabetes?"
> ❌ "Depression getting you down? Get help now."
> ❌ "Don't wait!! Get your spouse treated for cancer today with help from our medical experts."

"Does your baby have eczema?" is structurally identical to ❌ "Do you have diabetes?", and the third
❌ example is explicitly about a *family member*. **This copy is rejected on Meta.** The allowed shape
is the product-statement voice: "Baby eczema and food diary — log meals and skin, see the pattern."

The policy also states what is affirmatively permitted:

> Ads can: … Use "you/your" language without a personal attribute. … Make Public Service
> Announcements that inform the public about issues related to personal health attributes, as long
> as they don't assert someone or their family has a health condition.

### Health-claim review — the restricted category does **not** catch this product

Meta's [Health and Wellness](https://transparency.meta.com/policies/ad-standards/restricted-goods-services/health-wellness/)
restricted-goods policy opens:

> This policy covers two categories of ads: Weight Loss and Cosmetic Products and Procedures, and
> Adult Products and Reproductive Health.

Neither limb reaches an infant symptom diary. Notably the reproductive-health limb *does* enumerate
tracker apps as allowed with 18+ targeting ("Women's reproductive health apps, such as: Femtech apps,
Ovulation tracker, Pregnancy progress tracker") — evidence that Meta treats tracker apps as
advertisable, not as medical devices. A baby eczema tracker is outside that limb entirely, so no
written permission or certification applies.

### Spend

[How much it costs to advertise on Meta technologies](https://www.facebook.com/business/help/201828586525529):

> If you want to spend $5 a week, you can. If you want to spend $50,000 a week, you can do that too.
> Note: Some types of advanced ads require a minimum amount of spend to work.

No account minimum. Use an **account spending limit** as the hard $100 stop.

CPC: Meta publishes no benchmarks. Third-party 2026 aggregators put all-industry CPC around
$0.63–$1.72 and the Baby vertical at the low end of CPM (~$11.50) — *these are agency-blog numbers,
not Meta's*, and should be treated as order-of-magnitude only.

---

## Google Search — the recommended channel

### The crux: the restriction is on audiences, not keywords

[Restricted targeting in Personalized advertising](https://support.google.com/adspolicy/answer/143465)
lists Health among the sensitive interest categories, and states the restriction:

> Advertisers promoting products and services that fall within sensitive interest categories are
> unable to use advertiser-curated audiences. This helps ensure that sensitive interest categories
> aren't inadvertently used for targeting audiences.

> predefined Google audiences are expressly configured without sensitive user signals, so all
> advertisers are allowed to use them, even if they promote sensitive interest categories.

The enumerated restricted features are **Customer Match, Your data segments, Audience expansion,
Lookalike segments** — all audience products. **Keyword and contextual targeting are not on the
list.** Search ads match a query the user just typed; they are contextual, not personalized.

> **Caveat, flagged.** Google publishes no sentence saying "keywords are exempt." This is a strong
> inference from the policy's enumerated scope, not a quoted carve-out. Re-read the page before
> relying on it in writing.

The Health category is drawn wide, and deliberately reaches carers
([source](https://support.google.com/adspolicy/answer/16701855)):

> Content related to Health is a sensitive interest category and includes personal health content

with scope bullets covering "Physical or mental health conditions, including diseases, sexual health,
and chronic health conditions" and — the one aimed squarely at this product —

> Disabilities, even when content is oriented toward the user's primary caretaker

So the "the parent isn't the patient" argument does **not** buy an exemption from the audience
restriction. It just doesn't matter, because we aren't using an audience.

**Do not build a remarketing list (RLSA) off the waitlist page for eczema creative** — that is an
advertiser-curated audience and is caught.

**US vs UK:** the sensitive-category restriction reads as global with no regional carve-out. The only
region-scoped block on that page is "Access to opportunities" (housing/employment/credit), US and
Canada only. The UK delta is a *consent* obligation, not a targeting one — the
[EU user consent policy](https://www.google.com/about/company/user-consent-policy/) covers "the
European Economic Area, the UK and Switzerland" and requires consent for "the collection, sharing,
and use of personal data for personalization of ads." A UK Search-keyword test with no Google tag
largely sidesteps it; adding conversion tracking does not.

### Copy

[Data collection and use](https://support.google.com/adspolicy/answer/6020956) prohibits:

> Ads that imply knowledge of a user's personal information

Google's published example is financial — "You're buried in debt. Get help today." — structurally
identical to "Does your baby have eczema?". There is **no health-specific worked example** on the
page; the health application is an analogy from the rule's own wording. Flagged as inference.

### Certification: none

[Healthcare and medicines](https://support.google.com/adspolicy/answer/176031) requires certification
for prescription drug services, pharmaceutical manufacturers, US health/medical insurance, and
abortion-related queries in the US/UK/Ireland. The page contains **no mention of health apps, symptom
trackers, wellness apps, medical devices, or health information sites.** LegitScript attaches to
pharmacies, addiction services and telemedicine. A non-drug, non-clinical diary app trips none of it.

What *would* pull it in: a treatment or efficacy claim (eczema improvement, elimination-diet works),
or describing the app as diagnostic. Copy must stay on "record and see patterns," never "find the
trigger" as a promise.

### Spend

No stated account minimum (the `ads.google.com` FAQ is consent-gated and could not be fetched —
flagged). From [Set a budget that works for you](https://support.google.com/google-ads/answer/1704424):

> Your average daily budget is the amount you're willing to spend each day, on average, for each ad
> campaign in your account. The amount of your budget is entirely up to you

> Your actual spend on any given day may exceed your average daily budget by up to 2 times.

> You won't be charged more than your monthly charging limit, which is the average number of days in
> a month (30.4) multiplied by your average daily budget.

Set an [account spending limit](https://support.google.com/google-ads/answer/10486637) to $100 as the
hard stop; daily-budget math alone permits 2× overdelivery on any given day.

### CPC

Google publishes **no** industry benchmarks. The only authoritative first-party number available
pre-spend is Keyword Planner's top-of-page bid range
([metrics doc](https://support.google.com/google-ads/answer/3022575)): "an approximation of the 20th
percentile" and "the 80th percentile". **Run Keyword Planner on the actual keywords — it is free and
requires no spend.**

Third-party, labelled as such: WordStream 2026 puts all-industry Search CPC ~$5.42 and health &
wellness ~$1.63. Informational parent-intent terms ("baby eczema", "eczema on baby face") attract no
high-LTV bidder and plausibly run $0.50–2.00 US / £0.30–1.20 UK; commercial terms ("baby eczema
treatment", "eczema cream") draw DTC skincare money and run $2–6 US. **Bid informational, not
commercial.** Budget ~60–150 clicks total at $100 across both markets.

### The real rejection risk: the landing page

[Destination requirements](https://support.google.com/adspolicy/answer/6368661), *Insufficient
original content*, verbatim bullets:

> - Destination content that is designed for the primary purpose of showing ads
> - Destination content that is replicated from another source without adding value in the form of original content
> - Destinations that are solely designed to send users elsewhere
> - **Destinations that display a message of the destination not providing any services**
> - Destinations that are incomprehensible or don't make sense

The bolded bullet is a near-literal match for a "Coming soon — leave your email" page. Also:

> Destinations that don't function properly or have been set up incorrectly.

> Destinations that return an HTTP error code for Google AdsBot web crawlers on common devices globally.

**Checklist for the page:** substantive original copy about what the tracker records; no "coming soon"
as the primary message; a working form that confirms on submit; a privacy policy; display URL and
final URL on the same domain (no shortener, no off-domain redirect); **AdsBot not blocked in
`robots.txt`**; no dead App Store badge.

---

## TikTok

### Targeting: prohibited, and the prohibition is explicit

[Anti-Discrimination Ad Policy](https://ads.tiktok.com/help/article/tiktok-anti-discrimination-ad-policy?lang=en)
bars using audience tools to "wrongfully target specific groups of people for advertising" on
protected categories including:

> Individual health statuses or disabilities, including mental, physical, genetic, or emotional
> health and conditions

Note "familial status" is also a protected category, though TikTok plainly sells parenting interest
targeting (its own case studies use "Baby, Kids & Maternity"), so it does not read interest-in-baby-
products as familial-status discrimination.

Proxies available: [interest targeting](https://ads.tiktok.com/help/article/interest-targeting)
(taxonomy not published — verify in Ads Manager),
[behavior targeting](https://ads.tiktok.com/help/article/behavior-targeting?lang=en) (15-day video
actions, 90-day creator actions), hashtag/keyword targeting, and
[custom](https://ads.tiktok.com/help/article/custom-audiences)/[lookalike](https://ads.tiktok.com/help/article/lookalike-audience-faq?lang=en)
audiences — the latter needs "1,000 total matched users", so they are dead on arrival pre-launch.
Special Ad Categories are US/Canada housing-employment-credit only and do not apply.

### Copy: no equivalent rule exists — do not cite TikTok for one

**TikTok publishes no Meta-style personal-attributes ad-copy policy.** Searching the Ad Creatives and
Landing Page, Ad Format and Functionality, Anti-Discrimination, and Discrimination/Harassment pages
turns up no clause and no example naming second-person health phrasing. The nearest hooks are
[Ad Format and Functionality](https://ads.tiktok.com/help/article/tiktok-ads-policy-ad-format-and-functionality)
("must not disclose personal data or state or imply that the product can be used in a manner that
infringes an individual's privacy" — about the *product*, not the copy) and
[Discrimination, Harassment, and Bullying](https://ads.tiktok.com/help/article/discrimination-harassment-bullying)
(prohibits content that "Mocks or exploits individuals based on disability or health status").
"Does your baby have eczema?" is neither. It remains high-risk because TikTok runs
[keyword-level moderation](https://ads.tiktok.com/help/article/keyword-moderation-and-appeals-process?lang=en)
regardless of whether a written rule names the phrase.

### Healthcare industry review

[Healthcare and Pharmaceuticals](https://ads.tiktok.com/help/article/tiktok-ads-policy-healthcare-pharmaceuticals)
is organized as per-country prohibited/restricted lists. Prohibited: prescription medicine, elective
and weight-loss surgery, clinical trial recruitment. Restricted (needs "proof of approval and
certification from appropriate local regional regulating authorities"): OTC medicines, medical
devices, cosmetic clinics — all with 18+ targeting.

Findings from the document itself: **"United States" does not appear in it at all**; the UK appears
only inside a European bloc with unified requirements; and "eczema", "dermatitis", "symptom" and
"wellness" appear nowhere. The only tracking-app precedent is menstrual/ovulation apps, and only for
six Southeast Asian markets. So a diary app is *probably* an ordinary app ad in US/UK — **inference,
not a quotable permission.** Note "infant"/"baby" appear extensively regarding **infant formula and
baby food** restrictions: check the UK/EU bloc rules before any creative names a specific food.

### Spend — this is what disqualifies TikTok

[Budget](https://ads.tiktok.com/help/article/budget), verbatim minimums:

> Campaign daily budget: Budget must exceed $50
> Ad group daily budget: Budget must exceed $20
> Campaign lifetime budget: Budget must exceed $50
> Ad group lifetime budget: Minimum Budget = Total Days (including past days) × Minimum Daily Budget

$100 buys **five days in one market, one ad group**. Two ad groups (US + UK) hit a $40/day floor —
2.5 days, which is noise. Lifetime budget is a trap: a 14-day schedule demands $280 minimum. And
budget type cannot be changed after launch.

### Landing page

[Ad review checklist — landing page](https://ads.tiktok.com/help/article/ad-review-checklist-landing-page?lang=en):
pages must be functional, mobile-friendly, and "cannot request visitors provide sensitive information
to access the site" (the Ad Format policy expands this to health information). Pages must not be
"under construction" or "force downloads/personal data entry before accessing main content" — an
email-gate wall with nothing behind it is close to a literal match, and is the most likely rejection.
Ad and page must be consistent, so the ad must say "join the waitlist", not imply the app ships.

**Product-specific:** the waitlist form must ask for email only. Nothing about the baby's skin,
diagnosis or symptoms — that hits the sensitive-information clause, and TikTok separately bars lead
ads from collecting "Information concerning health" without written sales-rep consent.

### Children in creative

[Youth safety](https://ads.tiktok.com/help/article/tiktok-ads-policy-youth-safety): ads "must not
feature minors … in content that may put them at risk of sexual, physical, or emotional harm."
Featuring a baby is fine and standard in the vertical. **Clinical close-ups of inflamed infant skin
are the risk** — use illustration, UI screenshots, or a parent-facing shot. Set the ad group to 18+
regardless; it costs nothing and satisfies every health-adjacent 18+ default.

### CPC (third-party, TikTok publishes none)

US ~$10–14 CPM / ~$1.00–1.50 CPC; UK ~$6–10 CPM / ~$0.60–1.00 CPC. Agency-blog estimates only.

---

## Reddit

### Targeting — the community ban is the decisive line

[Targeting Guidelines](https://business.reddithelp.com/s/article/Reddit-Advertising-Policy-Targeting-Guidelines),
verbatim:

> These targeting rules apply to both positive targeting (i.e. including attributes) and negative
> targeting (i.e. excluding attributes).

> Reddit prohibits targeting users based on the following sensitive categories:
> … Genetic, biometric, or health data … Physical and mental health …

> You may not target communities in the following categories under any circumstance:
> - Addiction Support
> - Mature Themes and Adult Content
> - **Medical & Mental Health**
> - Trauma Support

The intuitive Reddit play — buy r/Eczema — is therefore the one thing explicitly forbidden. Reddit
does not publish its per-subreddit category map, so classification is enforced at review and is not
independently verifiable; **treat r/Eczema as prohibited.**

What *is* available ([Reddit audiences](https://business.reddithelp.com/s/article/reddit-audiences)):

> Community targeting: Communities ("subreddits") redditors subscribed to or have viewed or visited
> the communities in the last 28 days.

> When starting on Reddit, we recommend starting with interest targeting to broaden your audience.
> But if you'd like to use community targeting, try to include at least 15 communities per ad group
> for best results.

> Keyword targeting: Content containing keywords that you define. Note: This only supports terms in
> English.

Reddit *does* publish its interest taxonomy with bulk-import values, including **Family &
Relationships → Parenting (`parenthood_v3`)** and **Healthy Living → Diet & Nutrition
(`nutrition_v3`) / Wellness (`wellness_v3`)**, "based on the Interactive Advertising Bureau (IAB)
standard using classifications of communities that redditors subscribe to or visit."

Special ad categories are housing/employment/credit only
([About campaigns](https://business.reddithelp.com/s/article/about-campaigns)) and do not apply.

**Legal stack:** `Parenting` interest + ≥15 non-medical parenting communities (r/beyondthebump,
r/NewParents, r/Mommit, r/toddlers) + neutral keywords (`baby food diary`, `weaning`, `baby skin`).
Do not pair an `eczema` keyword with health-community targeting.

### Copy

Reddit has **no Meta-style personal-attributes prohibition.** The nearest text is one line in
[Editorial Requirements](https://business.reddithelp.com/s/article/Reddit-Advertising-Policy-Editorial-Requirements):

> Unless directed by law or regulatory authority, do not use personal information in your ad

So "Does your baby have eczema?" is not banned on its face here — it is a manual-review risk, and a
risk chiefly *by association with the targeting*. Prefer the neutral framing anyway.

### Spend — and a correction worth recording

**The widely repeated "$5/day Reddit minimum is not in the current help docs.** No minimum daily
budget and no minimum bid figure is published anywhere I could find (Budgets and Bidding, Standard
Campaigns, Simple Create, Purchase a Reddit Ad, all Billing articles checked). The only spend figure
Reddit currently documents is a *recommendation*
([Set up a campaign](https://business.reddithelp.com/s/article/Set-up-a-Reddit-Ads-Campaign)):

> Tip: Don't spread yourself too thin. Each ad group should have a daily budget of at least $50.

Which implies $100 buys roughly a **two-day burst in one ad group** on Reddit's own advice. Also
([How much do Reddit Ads cost](https://business.reddithelp.com/s/article/How-much-do-Reddit-Ads-cost)):

> Note: Since Reddit Ads relies on real-time, live auctions to deliver ads to users, your ad group
> may overspend its budget by up to 20%.

CPC (third-party, US-skewed, no UK parenting benchmark exists): median ~$1.25, consumer verticals
$0.10–0.80, CPM $3–12. Roughly 80–200 clicks for $100.

### Health-claim review

[Healthcare Products and Services](https://business.reddithelp.com/s/article/healthcare-products-and-services-policy):

> Reddit allows advertisements promoting healthcare products and services, with restrictions. …
> Advertisers must also take note of, and comply with, Reddit's policies on ad targeting.

> Some healthcare products and services require direct management from a Reddit Sales Representative.

A diary app is not a pharmaceutical, device, pharmacy, provider, supplement or telehealth service, so
no sales-rep-managed bucket applies — **provided no clinical claim is made.** The clause that bites
is the efficacy one: "Not imply prevention, diagnosis, or cure". Plus
[Deceptive, untrue or misleading](https://business.reddithelp.com/s/article/deceptive-untrue-or-misleading-advertising-policy):
"Making exaggerated claims without proof or evidence by a reasonable basis"; "Using overly
provocative or sensational content".

Landing-page clause from Editorial Requirements: "Advertised product and service on Reddit is
available on landing page" — **a pre-launch page must be honest that the product does not exist yet**,
or it risks this clause.

### UK availability

**No primary country list published** — flagged. Indirect primary evidence the UK is served: Reddit
maintains a UK-specific ad policy ("High Fat, Salt, Sugar Food and Drinks (UK)") and documents
country-level location targeting. Verify at signup; country selection fixes billing currency.

---

## Pinterest

### Targeting — the strictest of the five, because it bans proxies

[Advertising Guidelines](https://policy.pinterest.com/en/advertising-guidelines), "Be respectful with
your targeting", verbatim:

> **Don't target sensitive categories**
> Targeting certain audiences can be inappropriate and offensive. **It's never okay to target people
> in a way that implies you're aware of sensitive info about them.** You can't target any audience
> based on:
> - Sensitive health or medical condition
> - …
>
> **Please note that the targeting of proxies for the sensitive categories above is also not allowed.**

That proxy sentence is stricter than any other platform here. An interest or keyword set constructed
specifically to reach eczema parents is arguably the prohibited proxy. Scope is explicit:

> These advertising guidelines apply to all parts of your promoted content, including the image,
> description and destination—and they also apply to targeting features like keyword and audience
> targeting.

**Diary note:** the page carries a banner — "We're updating our Advertising Guidelines, effective
November 12, 2026." Re-read if the test slips past that date.

Available proxies: [interest targeting](https://help.pinterest.com/en/business/article/interest-targeting)
("based on their interests, tastes and life events" — taxonomy **not published**, visible only in Ads
Manager) and [keyword targeting](https://help.pinterest.com/en/business/article/keyword-targeting)
("reach people as they search for a specific idea"; "for the best results we recommend using at least
25 keywords per group"). Actalike audiences need a seed you don't have, and
[audience targeting](https://help.pinterest.com/en/business/article/audience-targeting) warns:
"Do not send Pinterest customer lists that are based on user activity from an app or website on an
iOS device. This includes lists that contain IDFA data." — directly relevant to an iOS product.

### Copy — two independent clauses reject it

Beyond the targeting clause above, Prohibited content → Sensitive content:

> Unless paired with educational or charitable information, we also don't allow content that
> capitalizes on controversial or tragic events or **references sensitive health or medical
> conditions**.

And in the data section:

> advertisers must not reference or ask via the Pinterest ads service for the following information
> related to sensitive categories: Sensitive health or medical condition, including related to
> genetics, fertility or pregnancy…

Because the guidelines cover "the image, description **and destination**", the **landing page copy is
in scope too**. Naming eczema anywhere in the funnel is likely rejectable. Pinterest is functionally
Meta's personal-attributes rule *plus* a ban on referencing the condition at all.

Also, lead ads are closed to this product outright:

> Advertisers promoting Pharmacy (Rx), Over-the-Counter (OTC) products, **health-related apps (e.g.,
> heart rate, weight)**, and/or Telehealth Services are prohibited from using lead ads.

Use a landing page, not a Pinterest lead ad.

### Spend

[Set your bid](https://help.pinterest.com/en/business/article/set-your-bid) — directly on point for a
US+UK test:

> Every campaign has a different bid floor, or minimum bid that's specific to a campaign or country.
> … For example, if you have a CPC campaign targeting US, UK, Canada, the bid floors are $0.10,
> £0.07, and $0.10 respectively. We convert these bid floors to USD then set the minimum as the
> highest price, which would be $0.10.

> Remember, you will only pay the minimum amount required at any given time no matter what you set
> your bid to.

**No minimum daily or lifetime budget is published** (checked `set-up-campaign-budgets`,
`manage-your-spend`, `campaign-details`) — flagged. Only relative guidance: "your daily budget should
be at least 5x your cost per result goal". Billing currency is locked at signup and cannot be edited
later.

CPC (third-party): ~$0.83 average, $0.30–1.50 range, parenting/home/CPG ~$0.30–0.80; CPM $2–10.
Roughly 125–330 clicks for $100 — the cheapest clicks of the five.

### Health-claim review

Advertising Guidelines → Healthcare products and services prohibits, among others:

> - Claims regarding the prevention or cure of disease
> - Products or advice we suspect could be unsafe, unreliable, or easily abused

The second is deliberately broad and is what a reviewer reaches for if the page implies the diary
identifies trigger foods. **Never claim the app finds, identifies or eliminates triggers.** The
Clickbait clause also bars "Playing on people's fear" and "Critiquing deficiencies".

US country-specific pre-approval covers pharma manufacturers, prescription drugs, online pharmacies
and prescription telehealth — none apply. UK country-specific guidelines list **only lotteries**, so
no UK healthcare restriction. Campaign review "can take up to 24 hours."

### UK availability — confirmed

[Promoted Pins overview](https://help.pinterest.com/en/business/article/promoted-pins-overview) lists
both the United Kingdom and the United States under "Advertisers in these countries can setup ad
accounts directly through Pinterest". Fully self-serve in both, no reseller.

---

## Recommendation

### The $100 goes to Google Search

**Why.** Every platform here restricts health as a *targeting signal*, but only Google separates the
restriction cleanly from the mechanism we actually want. Its sensitive-interest restriction is written
against **advertiser-curated audiences** — Customer Match, your data segments, audience expansion,
lookalikes — and keyword targeting is not in that enumerated list. So on Search we do not have to
build a proxy for "parent of an eczema baby" at all: the parent declares it themselves by typing
"baby eczema", and we buy the query, not the person. That sidesteps the entire problem the other four
platforms create, and it is the only channel where the reachable audience is *exactly* the audience
we want rather than a coarse parenting proxy.

Three practical reasons reinforce it:

1. **The budget works.** No account minimum, and an account spending limit gives a hard $100 stop.
   TikTok's published $50/day campaign and $20/day ad-group floors make $100 a five-day single-market
   test; Reddit's own advice asks for $50/day per ad group. Google is the only one where $100 buys a
   test across both markets over a sensible window.
2. **Intent quality.** 60–150 clicks of self-declared search intent is a far better signal for a
   validation question than 300 clicks of coarsely-targeted Pinterest browse traffic.
3. **No certification.** The Healthcare and medicines policy mentions no health apps, symptom
   trackers, wellness apps or health information sites. Nothing to apply for.

**How to run it.** Search only, no Display, no Search Partners. Two campaigns (US, UK) or one with
two ad groups, ~$3.50/day each over two weeks — but set the **account spending limit to $100**, since
daily budgets permit 2× overdelivery on any single day. Bid **informational** terms only ("baby
eczema", "baby eczema diary", "eczema food diary baby", "eczema on baby face"), never commercial ones
("baby eczema treatment", "eczema cream") — those draw DTC skincare money at $2–6. Pull Keyword
Planner's 20th/80th-percentile top-of-page bid range first; it is free and it is the only authoritative
pre-spend number that exists. **Do not build a remarketing list off the waitlist page** — RLSA is an
advertiser-curated audience and is caught by the restriction.

**Copy, in one rule that satisfies all five rulebooks.** Product-statement voice, third person, no
condition assigned to the reader, no efficacy claim:

> ✅ "Baby eczema and food diary — log meals and skin, spot the pattern."
> ✅ "A simple daily food and skin diary for babies."
> ❌ "Does your baby have eczema?"
> ❌ "Struggling with your baby's eczema? Find the trigger."

The first ❌ is a near-copy of Meta's own prohibited example ("Do you have diabetes?"). The second adds
an efficacy promise, which is what pulls Google and Reddit's health-claim clauses and Pinterest's
"unsafe, unreliable" clause into play. "Find the trigger" must never appear; "see the pattern" is the
safe form.

**Landing page is the real gate, not the health policy.** The single most likely rejection across all
five platforms is a thin coming-soon page, not the targeting. Google's *Insufficient original content*
bullet — "Destinations that display a message of the destination not providing any services" — is a
near-literal description of a bare email-capture page. So: substantive original copy about what the
tracker records, screenshots or mockups, a working form that confirms on submit, a privacy policy,
"join the waitlist" stated honestly (Reddit requires the advertised thing be *on* the page), display
URL and final URL on one domain, and **AdsBot not blocked in `robots.txt`**. Ask for **email only** —
nothing about the baby's skin, diagnosis or symptoms, which would hit TikTok's sensitive-information
clause and Pinterest's "must not reference or ask for" clause.

### Fallback if the Google ad is rejected

**Read the rejection reason first — it decides the fallback.**

- **Rejected for destination / insufficient original content:** this is not a channel problem. Fix
  the page and re-submit to Google. Every other platform has the same clause (TikTok "under
  construction", Reddit "available on landing page"), so switching channels does not help.
- **Rejected on policy grounds (personalized advertising, healthcare, misrepresentation):** go to
  **Reddit** with `Parenting` interest + ≥15 non-medical parenting communities and the neutral
  creative. Reddit is the best fallback because it has **no explicit personal-attributes copy rule
  and no proxy prohibition** — the two things that make Meta and Pinterest brittle — and its
  restriction is targeting-side and precisely bounded (don't buy Medical & Mental Health communities,
  which we weren't going to). Accept that $100 is a two-day burst there on Reddit's own guidance.
- **Second fallback: Meta**, product-statement copy only, parental-status + broad interest. It is
  cheap and has no minimum, but the copy rule is the sharpest of the five and the targeting taxonomy
  is actively being coarsened (exclusions gone Mar 2025; consolidation enforced Jan 15 2026).
- **Do not use Pinterest for this product.** It is the cheapest per click and the worst fit: the only
  platform that bans *proxies* for sensitive categories, bans ad content that merely *references* a
  health condition, extends both rules to the landing page, and specifically bars "health-related
  apps" from lead ads. There is no compliant way to say what this app is for on Pinterest.
- **Do not use TikTok at $100.** Not a policy problem — a budget one. The $20/day ad-group floor makes
  it a five-day one-market test, below the volume where its optimizer leaves the learning phase.

---

## What could not be verified from a primary source

- **Google:** no sentence exempting keywords from the sensitive-interest restriction (inferred from
  enumerated audience-product scope); no general health/wellness carve-out on the Health category
  page (absence is a finding, not a statement); no "no minimum spend" sentence; no health-specific
  example of the "imply knowledge of a user's personal information" rule.
- **Meta:** the detailed-targeting segment taxonomy is not published, so "Parents (All)" /
  "New parents (0-12 months)" must be confirmed in Ads Manager, not cited.
- **TikTok:** no personal-attributes copy rule exists (the "Does your baby have eczema?" prohibition
  is Meta's, not TikTok's — do not attribute it to TikTok); no US section in the healthcare policy;
  no published statement on health-tracking apps for US/UK; interest taxonomy unpublished; the
  Privacy Center "Ads and Your Data" page returns HTTP 403 to automated fetch, so TikTok's UK
  special-category position is unretrieved.
- **Reddit:** the commonly-cited $5/day minimum daily budget and any minimum bid figure are **absent
  from the live help docs** — only a $50/day *recommendation* exists. No supported-advertiser country
  list is published, so UK self-serve is inferred (from a UK-specific ad policy and country-level
  location targeting), not confirmed. The per-subreddit category map is not published, so r/Eczema's
  classification as "Medical & Mental Health" is a judgement call enforced at review.
- **Pinterest:** interest taxonomy not published; no minimum daily or lifetime budget published.
  The advertising guidelines are being **replaced effective 2026-11-12** — re-read before launch.
- **All platforms:** no first-party CPC benchmarks exist anywhere. Every CPC figure in this document
  is a third-party agency estimate except Google Keyword Planner's per-keyword top-of-page range,
  which is free to pull and is the only authoritative pre-spend number available.
- Meta's Transparency Center and several TikTok policy hubs render body text client-side and are not
  readable by automated fetch. Meta quotes here were taken from Internet Archive snapshots of the
  Meta-authored pages (Personal Attributes, 2026-06-09; Health and Wellness, 2026-07-10). Re-read the
  live pages before relying on exact wording.
</content>
