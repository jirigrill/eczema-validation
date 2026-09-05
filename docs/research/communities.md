# Where eczema parents gather, and what they say about tracking (US + UK)

Resolves [#2](https://github.com/jirigrill/eczema-validation/issues/2). All figures and quotes accessed **2026-09-05**. Every quote was copied from a page or API response actually retrieved on that date and carries a direct link. Where a number could not be obtained from a reachable source, that is stated rather than estimated.

## Headline

The venues exist and are large, but **the complaint the product is built around is not the complaint parents voice.** Across ~909 Netmums / patient.info / HealthUnlocked threads (2007–2021) and ~1,300 archived Reddit comments from eleven parenting and eczema subreddits, the food diary appears overwhelmingly as **advice given** — by health visitors, GPs, dietitians and other parents — and almost never as a practice a parent reports as having worked. The dominant verbatim pattern is not "logging is tedious"; it is **"I kept the diary and it told me nothing."**

Two further measured facts sharpen this. First, in that entire non-Reddit corpus there is **not one mention of an eczema app, a symptom-tracking app, a spreadsheet, or the Notes app** — the stack is paper, reactive phone photos taken for a clinician, and memory. Second, the closest thing to an incumbent, the **National Eczema Association's own EczemaWise tracker, is being shut down**: "EczemaWise will be sunsetting on December 18, 2026. New user sign-ups are now disabled." ([App Store listing](https://apps.apple.com/us/app/eczemawise-eczema-skin-care/id1522743215), developer: National Eczema Association). Its Google Play listing shows **5K+ downloads, 4.1 stars, 57 reviews** ([Google Play](https://play.google.com/store/apps/details?id=com.eczemawiseapp&hl=en_US)) — the official US patient-charity tracker, retired at five thousand Android installs.

This corroborates [#4](https://github.com/jirigrill/eczema-validation/issues/4) from a completely different direction: that ticket found no measurable *search* demand for food-trigger tracking; this one finds no *spoken* demand for it either. Parents want the trigger identified, not the diary improved.

## Method and its limits — read before using anything below

| Source | How reached | What it yields |
|---|---|---|
| **Arctic Shift** (`arctic-shift.photon-reddit.com/api`), a public archive of Reddit's own API responses | called directly with `curl`; endpoints `comments/search`, `posts/search`, `posts/ids`, `comments/tree`, `subreddits/search` | verbatim Reddit comment/post bodies with permalinks, subscriber counts, post metadata |
| Netmums, patient.info, HealthUnlocked, Facebook Pages, Instagram tag pages | direct HTTP fetch of public thread URLs | verbatim forum posts; `og:description` counts |
| Apple App Store, Google Play | fetched listing pages | app sunset notices, ratings, install bands |
| Wayback Machine | `web.archive.org` snapshots, snapshot id given in place | policy text whose live URL now 403s or 400s |

**Reddit itself is not directly fetchable from this machine.** `reddit.com`, `old.reddit.com` and `api.reddit.com` all return the login/bot-check shell to `curl`; the agent fetcher refuses `www.reddit.com` outright; six Redlib/Libreddit mirrors were tried and returned 403, 418 or an Anubis proof-of-work wall. **Every Reddit fact below therefore comes from the Arctic Shift archive, not from Reddit.** Two consequences:

1. **Subscriber counts are a snapshot taken 2025-02-14/15** — the most recent subreddit metadata the archive holds. They are ~19 months stale as of 2026-09-05 and are almost certainly low. Treat them as floors, and re-check by hand before quoting them anywhere external.
2. **Subreddit rules could not be read.** `reddit.com/r/<sub>/about/rules/` is unreachable by every route tried, and r/eczema's sidebar simply points at it ("**Subreddit Rules:** [See here](https://www.reddit.com/r/eczema/about/rules/)" — archived sidebar text). So the self-promotion column for Reddit is filled **empirically** — from whether comparable posts actually survived moderation — not from rule text. That is weaker evidence about the rule and stronger evidence about the outcome; it is flagged as such in the table.

Two more limits worth carrying:

- **Arctic Shift's full-text search times out under load.** Roughly 60% of `comments/search` calls with `limit=100` returned `422 {"error":"Timeout. Maybe slow down a bit"}`; dropping to `limit=20–30` helped but did not eliminate it. The Reddit quote set below is therefore a **non-random sample of what the archive would serve**, not an exhaustive sweep. Absence of a phrase in my results is not evidence of absence on Reddit.
- **Netmums, HealthUnlocked and Inspire refuse the agent fetcher** (robots/403) and were read by direct HTTP instead. The text is verbatim and the URLs are real, but the material was obtained against those sites' stated crawler preference. That matters if any of it is quoted publicly.
- I **spot-verified three** of the non-Reddit quotes myself by re-fetching the thread and finding the exact string (Netmums 1254503, patient.info 760239, HealthUnlocked 150379914). All three matched exactly. The remainder come from a sub-agent's crawl of pages it fetched.

---

## Venue table — Reddit

Sizes are Arctic Shift's archived value of Reddit's own `subscribers` field, snapshot date given. "Posts retrieved" is how many posts matching the given title term the archive served me — a rough activity signal, **capped at 100 per query**, so any figure of exactly 100 is a floor, not a count.

| Venue | Subscribers (2025-02-14/15 snapshot) | Activity signal | Self-promotion / research-recruitment | Link |
|---|---|---|---|---|
| **r/eczema** | 105,807 | 529 posts retrieved with `baby` / `daughter` / `newborn` / `diet` in the title (three of those queries hit the 100 cap). Condition-specific and the single best-matched venue. | Rules page unreachable. **Empirically permissive**: a founder's post *"Looking to interview parents who have kids with eczema"* (2026-06-21) was **not removed** — but scored **1 point and 2 comments**. Sidebar carries a medical disclaimer and "do not post pictures asking for a diagnosis"; posting is restricted (`restrict_posting: true`). | [r/eczema](https://www.reddit.com/r/eczema/) · [the founder post](https://www.reddit.com/r/eczema/comments/1ubekg0/looking_to_interview_parents_who_have_kids_with/) |
| **r/EczemaUK** | 2,787 | 45 posts retrieved across all title terms tried, **17 in 2025 and 15 in 2026** — a handful of posts a month at best. | Not measurable at this volume. | [r/EczemaUK](https://www.reddit.com/r/EczemaUK/) |
| **r/beyondthebump** | 736,426 | 100+ posts with `eczema` in the title; the largest single eczema thread found anywhere on Reddit is here — *"I feel destroyed by my baby's eczema"*, **59 points, 120 comments**. | **Empirically permissive but commercially dead**: *"I was struggling, so I built an app to help figure out what was triggering my granddaughter's eczema"* (2026-07-06) was **not removed** and scored **0 points, 1 comment**. | [r/beyondthebump](https://www.reddit.com/r/beyondthebump/) · [the app post](https://www.reddit.com/r/beyondthebump/comments/1up1b67/i_was_struggling_so_i_built_an_app_to_help_figure/) · [the 120-comment thread](https://www.reddit.com/r/beyondthebump/comments/1lggfd7/i_feel_destroyed_by_my_babys_eczema_is_there/) |
| **r/NewParents** | 374,722 | Active on tracking *in general* — an August 2026 thread *"Who is using newborn tracking apps? Why or why not?"* drew a long comment run. Eczema-specific volume much lower. | Rules unreachable; not measured. Note that the tracking-apps thread itself contains several unprompted app plugs that were not removed. | [r/NewParents](https://www.reddit.com/r/NewParents/) · [tracking-apps thread](https://www.reddit.com/r/NewParents/comments/1vz1b18/who_is_using_newborn_tracking_apps_why_or_why_not/) |
| **r/FoodAllergies** | 22,066 | Small but the **highest-density source of food-diary language found anywhere**, including the breastfeeding-elimination cohort. | Rules unreachable. A founder comment *"I know this is an old post but I'm building an app for this exact use case"* (2025-08) survives in the archive. | [r/FoodAllergies](https://www.reddit.com/r/FoodAllergies/) |
| **r/Parenting** | 8,056,434 | Largest venue by far; eczema content proportionally rare. | Rules unreachable; not measured. | [r/Parenting](https://www.reddit.com/r/Parenting/) |
| **r/Mommit** | 2,596,695 | Eczema-specific volume low; general "how do you keep track of feeding" threads active. | Rules unreachable; not measured. | [r/Mommit](https://www.reddit.com/r/Mommit/) |
| **r/toddlers** | 442,542 | Low eczema volume in retrieved sample. | Not measured. | [r/toddlers](https://www.reddit.com/r/toddlers/) |
| **r/breastfeeding** | 179,738 | Relevant to the elimination-diet-while-nursing cohort specifically. | Not measured. | [r/breastfeeding](https://www.reddit.com/r/breastfeeding/) |
| **r/ScienceBasedParenting** | 167,776 | Low eczema volume; audience wants citations. | Not measured. | [r/ScienceBasedParenting](https://www.reddit.com/r/ScienceBasedParenting/) |
| **r/daddit** | not retrieved | 42 posts with `eczema` in the title, spread 2015–2026 (10 in 2024, 12 in 2025). | Not measured. | [r/daddit](https://www.reddit.com/r/daddit/) |

**The one thing the Reddit column says clearly.** Two separate people ran this exact play in 2026 — one recruiting parents for interviews in r/eczema, one launching an eczema-trigger app in r/beyondthebump — and **neither was moderated away, and neither got any traction**. Combined scores across both posts: 1 point, 3 comments. Whatever the rules say, the outcome is the same: posting into these subreddits is permitted and near-worthless.

---

## Venue table — Facebook, Instagram, TikTok

| Venue | Size | Activity | Self-promotion rules | Link |
|---|---|---|---|---|
| **National Eczema Association** (FB Page, US) | **66,250** likes | 138 "talking about this" | Meta Community Standards only; no page-level rule published | [facebook.com/nationaleczema](https://www.facebook.com/nationaleczema/) |
| **National Eczema Society / Eczema UK** (FB Page) | **29,740** likes | **172** "talking about this" — *more* than NEA on under half the likes | Meta Community Standards only | [facebook.com/eczemasociety](https://www.facebook.com/eczemasociety/) |
| **Eczema Outreach Support** (FB Page, UK) | **5,451** likes | 22 "talking about this" | See EOS row in the charity table | [facebook.com/eczemaoutreachsupport](https://www.facebook.com/eczemaoutreachsupport/) |
| **Facebook groups** (Eczema Support Group `/MyEczema/`, Eczema Parents, UK Eczema Support, HappySkin Community) | **unverified — every `facebook.com/groups/*` URL 302s to `/login/` and returns HTTP 400**, tried under three user agents | unverified | **Group rules live inside the login wall and are not fetchable.** Facebook's own help page on group rules (`facebook.com/help/1210322209008185`) also returns 400 unauthenticated. | [/groups/MyEczema/](https://www.facebook.com/groups/MyEczema/) · [UK Eczema Support](https://www.facebook.com/groups/1409148029366627/) · [HappySkin Community](https://www.facebook.com/groups/961075527629777) |
| **Instagram hashtags** | **#eczemababy 340K reels**, **#babyeczema 216K reels**, **#eczemahealing 209K reels**, **#eczemamom 45K reels** — read from each tag page's `og:description` (exact string form: `content="Babyeczema • 216K reels on Instagram"`). #eczemakids, #atopicdermatitis, #eczemawarrior, #eczemamum, #eczemamama, #eczemachild, #eczemafree, #babyeczemarelief, #eczemaparents all returned the generic login wall — **not verifiable**. | not measurable without login | Meta Community Standards govern Instagram (`help.instagram.com/477434105621119` now 301s to the Meta page); Meta Branded Content Policies require the branded-content tool plus "all necessary disclosures to people using Facebook or Instagram" | [#babyeczema](https://www.instagram.com/explore/tags/babyeczema/) |
| **TikTok hashtags** | **no count obtained at all** — `tiktok.com` returns 403 through two independent network paths (a corporate Zscaler proxy on this machine, and the agent fetcher separately). Measuring TikTok needs a logged-in human. | unknown | **Strict, and stricter than most assume** — see the verbatim block below | [tiktok.com/tag/babyeczema](https://www.tiktok.com/tag/babyeczema) |

**A texture point before treating the big Facebook groups as neutral ground.** The Wayback `og:description` for `/groups/MyEczema/about/` (snapshot 2024-03-06) is itself a merch pitch: *"Get some Eczema Warrior/Awareness products such as t-shirts, health warrior merch, magnets, stickers, and assistance cards…"* — the largest listed eczema group describes itself with a link to a store.

**Third-party group sizes, clearly labelled as such.** Healthline (page updated 2024-01-09, ~20 months stale) lists Eczema Support Group as "65,000+, Private" and Eczema Parents as "11,000+, Private". **Never observed on Facebook itself** — do not present as current.

### TikTok rules, quoted verbatim

TikTok Community Guidelines, "Commercial Disclosure and Paid Marketing" — live URL 403s; recovered from Wayback snapshot `20260101062824` of `tiktok.com/community-guidelines/en/regulated-commercial-activities`, page states "Released August 14, 2025 / Effective September 13, 2025":

> "If you're posting commercial content on TikTok, you must clearly disclose it using the content disclosure setting. This helps people understand when you're marketing something.
>
> Disclosure is required when you're:
> Promoting your own business, product, or service
> Posting branded content, including reviews or endorsements, and receiving any kind of incentive in exchange"

> "If commercial content isn't disclosed using the content disclosure setting, it will be ineligible for the FYF. If we find commercial content that hasn't been properly disclosed, we may apply the content disclosure setting or remove it from the FYF. Repeated failure to make a disclosure can lead to your account being temporarily restricted from posting content, or can lead to an account ban."

The load-bearing limb is **"Promoting your own business, product, or service"** — posting about your own app requires the disclosure toggle even with no brand deal and no money changing hands.

TikTok's own detection description ([ads.tiktok.com help article](https://ads.tiktok.com/help/article/about-the-content-disclosure-setting-for-creators), fetched live, "Last updated: April 2026"):

> "TikTok flags videos as commercial content when it shows clear marketing intent based on three factors: **Financial incentives:** … **Brand mentions:** When a brand's name appears as a hashtag (#brand), a tag (@brand), or a logo is shown. **Product recommendations:** Showing or talking about a product or service, such as demos, tutorials. This could also include calls to actions, such as buy now or shop today."

> "You'll receive a notification if your video potentially contains branded content but is not following proper disclosure. Then you'll have the opportunity to respond to suspected branded content system notifications within 24 hours before the video is ineligible for the For You Feed."

TikTok Branded Content Policy (Wayback `20251225130054` of `tiktok.com/legal/page/global/bc-policy/en`) additionally forbids content that would:

> "cause physical, mental, or moral detriment to minors; exhort minors to buy, rent, or hire a product or service, or encourage minors to persuade their parents or others to purchase goods or services being advertised; or exploit the trust minors place in parents, teachers, or other persons"

### Meta rules, quoted verbatim

Meta Community Standards, Spam (Wayback `20251217072045`; the standards "outline what is and isn't allowed on Facebook, Instagram, Messenger and Threads"):

> "We do not allow content that is designed to deceive, mislead, or overwhelm users in order to artificially increase viewership. This content detracts from people's ability to engage authentically on our platforms and can threaten the security, stability and usability of our services."

> "**Misleading Links**: Content containing a link that promises one type of content but delivers something substantially different. This can include content in a promised app or software."

Meta Branded Content Policies (live URL 400s; Wayback `20250930073238` of `facebook.com/business/help/221149188908254`):

> "We define branded content as a creator or publisher's content that features or is influenced by a business partner for an exchange of value, such as monetary payment or free gifts. Branded content may only be posted with the use of the branded content tool…"

---

## Venue table — charities and parenting forums

| Venue | Size (as published by the venue) | Activity | Self-promotion / research rules | Link |
|---|---|---|---|---|
| **National Eczema Association (US)** | "1 million monthly global page views and over 75K email subscribers" | Blog, webinars, Eczema Expo, Ambassadors, Eczema Awareness Month. Its page sitemap contains **no forum or community board** — community is off-site (social) plus events | Not a forum, so no poster rules. Two **paid** routes exist instead: **PEER** (fee-for-service research recruitment) and advertising/sponsorship | [advertising-sponsorship](https://nationaleczema.org/advertising-sponsorship/) · [recruit-eczema-patients](https://nationaleczema.org/recruit-eczema-patients/) · [page-sitemap.xml](https://nationaleczema.org/page-sitemap.xml) |
| **EczemaWise** (NEA's app) | 5K+ Android downloads, 4.1★, 57 reviews (Google Play); 4.6★, 217 ratings (App Store) | A tracker, not a venue. **Registration closed 2026-04-15; sunsets 2026-12-18** | n/a | [eczemawise.org](https://www.eczemawise.org/) · [App Store](https://apps.apple.com/us/app/eczemawise-eczema-skin-care/id1522743215) |
| **Inspire "Eczema Exchange"** (third-party, not NEA-run) | **No member count exposed** on any readable snapshot | 8 topic areas including **"Parents, friends and family"**; ~10 discussions, all adult-focused (Dupixent, TSW) — **no parent or food-tracking content** | **The hardest ban of any venue here** — bans promoting a product/app *and* recruiting for market research or surveys, and commercial entities may not even register | [Wayback 2023-03-30](http://web.archive.org/web/20230330072041/https://www.inspire.com/groups/eczema-exchange/) · [guidelines, Wayback 2024-02-06](http://web.archive.org/web/20240206220718/https://www.inspire.com/about/guidelines/) |
| **National Eczema Society → now "Eczema UK"** (`eczema.org` 302s to `eczema.org.uk`) | Membership £25/yr UK; "39 EXEC group members"; "£256K in research grants in 2025" | **Runs no forum.** Channels: *Exchange* magazine, monthly e-newsletter, webinars, AGM, EXEC patient-expert group | No forum ⇒ no posting rules. Research listings are staff-curated, with a disclaimer that listed projects "are not run by Eczema UK" | [membership](https://www.eczema.org.uk/get-involved/membership) · [impact](https://www.eczema.org.uk/impact) · [take part in research](https://www.eczema.org.uk/research/take-part-in-eczema-research) |
| **Eczema Outreach Support (UK)** | **"836 new families joined"** (Apr 24 – Mar 25); income £270,584; Scottish charity SC042392; FB Page 5,451 likes | **Closed Facebook group** (service users only), monthly "Grab a Cuppa" Zoom for carers, High 5 Kids Club (7–12), Youth Panel (16–25), 1:1 calls, family events | **Gated** — you must register via the "Get Support" form to reach families. No published external-researcher process; phone/email only | [our work in numbers](https://eos.org.uk/our-work-in-numbers/) · [parents and carers](https://eos.org.uk/parents-and-carers/) · [research](https://eos.org.uk/get-involved-with-eczema-research/) |
| **Allergy UK** | "21 million people in the UK live with allergic disease" — a population stat, **not an audience figure** | **No forum.** Helpline (01322 619898), web chat, monthly eNews, Allergy Alerts, Youth Engagement Group | No forum ⇒ no poster rules; access is via helpline/newsletter partnership | [allergyuk.org](https://www.allergyuk.org/) |
| **Anaphylaxis UK** | No membership figures published | **No forum.** Newsletter, training, "Get involved in research". Live site was **down for maintenance** on 2026-09-05 | none published | [Wayback 2025-04-17](http://web.archive.org/web/20250417203649/https://www.anaphylaxis.org.uk/about-us/) |
| **Mumsnet Talk** | "around 8 million unique visitors per month" and "around 100 million page views"; ad site claims "25,000 posts daily" and "1 in 3 adult women aged 35-54" | **Allergies & Food Intolerances board = 227 pages of threads, top threads updated same-day.** The single highest-value UK venue for this ICP | Spam-promotion of your own product, service **or survey** is deleted. Designated paid lane: **Non-member requests board, £30 fee.** Charity fundraising only for registered charities. Journalists route via a moderator email | [netiquette](https://www.mumsnet.com/i/netiquette) · [about us](https://www.mumsnet.com/i/about-us) · [/talk/allergies](https://www.mumsnet.com/talk/allergies) · [/talk/nonmember_requests](https://www.mumsnet.com/talk/nonmember_requests) |
| **Netmums Coffeehouse** | "welcoming millions of parents every month"; "over 1.3million social media followers"; 150 local sites | ~26 board groups including `health-wellbeing-1087` and `special-needs-and-disabilities`. Registration required to post; **not pre-moderated**. The eczema/allergy threads mined below are almost all from here | Rule 10: you may state your professional background but must not use the boards "as a way of promoting or advertising any services, business or website". Rule 4 bans MLM. Designated lane: **"Media and research requests"** board, with a *Take part in research* sub-board | [chat rules](https://www.netmums.com/info/chat-rules) · [about us](https://www.netmums.com/info/about-us) · [media & research requests](https://www.netmums.com/coffeehouse/media-research-requests-1176/) |
| **What to Expect community** | **No size figure could be attributed** — see blocked-sites note | Group directory spans Getting Pregnant / Pregnancy / First Year / Family Health / International | Terms §4 bans "junk mail, spam or unauthorized advertising or promotional materials, including … links to commercial products or services". §5 requires citing sources for health claims not from personal experience | [terms of use](https://www.whattoexpect.com/terms-of-use/) |
| **BabyCenter community** | "more than 50 million parents visit BabyCenter's 11 websites every month" (**2021 snapshot** — treat as vintage) | Birth Clubs, Groups, Topics, Mom Answers; explicitly *not* monitored because "our community is so large" | Rule 8: "No soliciting, advertising or marketing, except in designated spaces." (guidelines page footer dates itself **2009**) | [guidelines, Wayback 2020-03-10](http://web.archive.org/web/20200310063451/https://www.babycenter.com/0_babycenter-community-guidelines_10415873.bc) · [about, Wayback 2021-04-09](http://web.archive.org/web/20210409233344/https://www.babycenter.com/about-babycenter) |
| **patient.info Patient Communities** (Discourse) | **414,785 users; 488,553 topics; 3,022,100 posts; 484 active users/30d; 126,208 visitors/30d.** *Skin, nail and hair health* 7,156 topics / 44,374 posts; *Allergies, blood and immune system* 5,049 / 41,895; *Children's health* only 382 / 1,961 | Live daily (165 topics + 171 posts in the last day at time of fetch). Eczema threads sit in *Skin, nail and hair health* | Terms: "You may not send advertisements, chain letters, or other solicitations through the forum, or use the forum to gather addresses or other personal data for commercial mailing lists or databases." No `/guidelines` page exists | [about.json](https://community.patient.info/about.json) · [categories.json](https://community.patient.info/categories.json) · [tos](https://community.patient.info/tos) |
| **HealthUnlocked** | **No eczema or allergy-charity community exists.** Nearest: MY SKIN **9,234** members; Eczema Association of Australasia **460**; CMPA (cow's-milk protein allergy) **315**; Asthma Community Forum 24,871. (Scale reference: Thyroid UK 152,542) | Eczema talk is scattered as posts inside unrelated communities | **No verbatim rule quote available** — `/terms`, `/terms-of-use` and `/code-of-conduct` all 404 and the homepage renders links client-side | [community search API](https://solaris.healthunlocked.com/search/communities?q=eczema) · [directory](https://healthunlocked.com/communities) |

**The sanctioned lanes are worth naming, because most of these venues have one.** Mumsnet sells it outright (£30 per post on the Non-member requests board); Netmums runs a *Take part in research* sub-board; NEA runs PEER as a fee-for-service; Eczema UK and EOS both publish staff-curated pages of studies recruiting families. **Inspire is the only flat, unconditional ban** — it prohibits promotion *and* survey recruitment *and* refuses registration to commercial entities at all.

### Rules quoted verbatim

**Mumsnet — Netiquette / Talk Guidelines** — [mumsnet.com/i/netiquette](https://www.mumsnet.com/i/netiquette)

> "We have no problem with people posting the odd link to other sites/blogs that other posters might find useful or interesting."

> "We'll delete anyone's attempts to spam the boards with links, as a way of promoting their own product, services, survey or e-petition."

> "Non-members looking for MN users' input can post on our Non-member requests board for a £30 fee."

> "We only allow fundraising for registered charities to be promoted on our Talk boards - and these threads should be posted on the charities noticeboard."

**Mumsnet — Non-member requests board description** — [mumsnet.com/talk/nonmember_requests](https://www.mumsnet.com/talk/nonmember_requests)

> "This topic is for non-members looking for MN users' input; there is a £30 fee."

**Netmums — Forum Chat Rules, rule 10 "Posting as a professional"** — [netmums.com/info/chat-rules](https://www.netmums.com/info/chat-rules)

> "While you are welcome to state your current/previous professional expertise, you should not use our boards as a way of promoting or advertising any services, business or website provided or used by yourself or others."

**Netmums — rule 4** (same URL)

> "Netmums does not support MLM Companies (multi-level marketing) and we do not allow the promotion of them on our Forum. The Netmums Forum is not pre-moderated, but our team of moderators WILL delete MLM posts as they find them, anyone can report them to the moderators to be deleted."

**What to Expect (Everyday Health) — Terms of Use §4 Prohibited Activities** — [whattoexpect.com/terms-of-use](https://www.whattoexpect.com/terms-of-use/)

> "Post statements or materials that constitute junk mail, spam or unauthorized advertising or promotional materials, including, without limitation, links to commercial products or services or any political campaigning;"

**What to Expect — Terms of Use §5 Message Boards** (same URL)

> "Post honest and valuable information and don't post rumors or negative opinions that are not supported by facts. Unless the information in your post arises directly from your personal experience, references to any health-related or medical information you provide must be included in your post."

**BabyCenter — Community Guidelines, "The Rules"** — Wayback snapshot 2020-03-10; page footer says "Last updated: June 29, 2009" — [snapshot](http://web.archive.org/web/20200310063451/https://www.babycenter.com/0_babycenter-community-guidelines_10415873.bc)

> "8. No soliciting, advertising or marketing, except in designated spaces."

> "Because our community is so large, BabyCenter doesn't monitor or verify the information posted by our members."

> "Group owners may place supplemental rules within their group; those rules do not override the community guidelines and BabyCenter Staff will not enforce those supplemental rules."

**Inspire — Community Guidelines, "No commercial use, promotion or solicitation"** — Wayback snapshot 2024-02-06 — [snapshot](http://web.archive.org/web/20240206220718/https://www.inspire.com/about/guidelines/)

> "You may not use Inspire for any commercial purpose, marketing, promotion, or solicitation. This includes promoting a company, product, service, person, treatment, therapy, Web site, support group, non-profit, charity, or fundraiser; recruiting members to participate in market research, clinical studies, or surveys; soliciting donations for charitable causes or for yourself; presenting your resume or using Inspire to seek employment; and soliciting clients. Commercial entities are not permitted to sign up or create profiles on Inspire."

**patient.info Patient Communities — Terms, "Acceptable Use"** — [community.patient.info/tos](https://community.patient.info/tos)

> "You may not send advertisements, chain letters, or other solicitations through the forum, or use the forum to gather addresses or other personal data for commercial mailing lists or databases."

**National Eczema Association — PEER, the paid recruitment route** — [nationaleczema.org/recruit-eczema-patients](https://nationaleczema.org/recruit-eczema-patients/)

> "We offer PEER, or People Engaged in Eczema Research, a fee-for-service program that helps researchers and clinicians promote their clinical trial and research study to relevant eczema patients and caregivers."

**National Eczema Association — audience size** — [nationaleczema.org/advertising-sponsorship](https://nationaleczema.org/advertising-sponsorship/)

> "With 1 million monthly global page views and over 75K email subscribers and growing, NEA is positioned to get your brand in front of a deeply engaged eczema community."

**Eczema Outreach Support — the closed Facebook group** — [eos.org.uk/parents-and-carers](https://eos.org.uk/parents-and-carers/)

> "a safe place for you to share your experiences, support each other and share hints and tips around living with eczema in the family"

### Sites that blocked retrieval, stated explicitly

- **netmums.com, whattoexpect.com, babycenter.com** all refuse the agent fetcher. Netmums' own `robots.txt` allows general crawling, so it was read directly. **Ziff Davis's `robots.txt` on whattoexpect.com and babycenter.com explicitly prohibits automated retrieval for AI purposes** — the What to Expect Terms page had already been retrieved before that file was read; BabyCenter was taken from Wayback instead. Treat BabyCenter's numbers as 2021-vintage and its guidelines as 2009-vintage.
- **inspire.com** — CloudFront 403 on every live URL, and 403 on several Wayback replays. Usable snapshots: 2023-03-30 and 2024-02-06.
- **healthunlocked.com** — 403 to the agent fetcher; client-rendered. Clean membership data came from its own public search API, but **the Terms / Code of conduct page could not be located** (all candidate URLs 404), so there is no verbatim HU rule quote.
- **anaphylaxis.org.uk** — live site returned "down for maintenance" on 2026-09-05; Wayback 2025-04-17 used instead.
- **`eczema.org` 302s to `eczema.org.uk`** — the National Eczema Society now brands as **"Eczema UK"**. Research written against `eczema.org` will hit the wrong hostname.

### What is confirmed dead or unreachable

Recorded so the next agent does not spend the time again:

| Venue | Status on 2026-09-05 |
|---|---|
| `nationaleczema.org/eczema-wise/` | **404.** NEA has restructured; four plausible community URLs all 404'd. No first-party NEA online community could be confirmed beyond social media. |
| `eczemawise.org` | App landing page, JavaScript-only, no public community. Registration closed 2026-04-15; app sunsets **2026-12-18**. |
| Inspire "Eczema Exchange" (`inspire.com/groups/eczema-exchange/`) | The de-facto US eczema forum. **~10 discussions, all adult-focused** (Dupixent, TSW, osteoporosis). **No parent or food-tracking content exists there.** Member count is login-gated; the widely-cited 33,000 figure traces to HealthCentral, which blocked fetching. |
| `eczema.org` (National Eczema Society, UK), `allergyuk.org` | **No public forum exists.** Helplines and facilitated video groups instead. |
| Eczema Outreach Support Facebook group | Service-user gated: "Families are given access to the closed group once they have become service users of EOS" ([eos.org.uk/parents-and-carers/](https://eos.org.uk/parents-and-carers/)). Not a venue you post into — a venue you enter through the charity. |
| `kidswithfoodallergies.org` | Blogs readable, zero comments; all member topics 302 to a sign-in wall. |
| whattoexpect.com | Blocked. No quotes obtainable. |
| community.babycenter.com | Raw HTML fetches, but search and posts are client-rendered with no discoverable API. No quotes. |
| madeformums.com | Redirects to `tollbit.madeformums.com`, which returns **502**. |
| babyandbump | **403**. |
| emmasdiary.co.uk/community, bounty.com/community | **404** — no forum. |
| talkhealth Partnership | **Defunct** — "This website is no longer available". |
| allergymoms.com | **No longer resolves.** |

**The pattern in the UK charity column is structural, not incidental.** Allergy UK, Anaphylaxis UK, EOS and the National Eczema Society all run helplines and facilitated video calls rather than searchable forums. Reach there is relationship-mediated: you get in by becoming a service user or by being listed on a research page, not by posting. **EOS is the tightest population match** — UK, children birth to 18, families, 836 new families in a year — and the most open to research participation.

---

# The quotes

Grouped by the complaint they express. Every quote is verbatim, including its original typos and punctuation. Reddit quotes come from the Arctic Shift archive of Reddit's API; forum quotes from direct fetches of the linked thread.

## 1. "I kept the diary and it told me nothing"

This is the largest group by a wide margin, and it is the finding that should change the product thesis. The diary is not failing because it is hard to fill in. It is failing because **filling it in correctly still yields no answer.**

> "Keeping a food diary now but can't seem to find an obvious trigger though chocolate makes it worse."
> — Eloquentia, 2024-01-04, HealthUnlocked, Pregnancy and Parenting Support — [link](https://healthunlocked.com/pregnancy-parenting-support/posts/150379914/eczema)

> "I even kept a food diary and can't figure out a connection. Somehow, spring (pollen) seems to make it worse. It's never gone."
> — 2015-04-06, patient.info — [link](https://community.patient.info/t/suggestions-for-child-with-eczema/398191)

> "I can't seem to pin down what is flaring it up, I've kept food diaries and tried cutting out dairy altogether but this didn't seem to help. I thought I had cracked it when he had icecream one day and it really flared up, but I think it must have been a coincidence."
> — 2021-04-18, patient.info — [link](https://community.patient.info/t/please-help-toddler-face-rash/760239)

> "I did keep a very detailed food diary during most of December, but it is very difficult to list every single ingredient and there was no severe reaction during this time period."
> — Ela79kuv, 2009-02-25, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/260685-please-help-possible-food-allergy.html)

> "This really helped us as I was Breastfeeding DS1 at the time and I did a food diary to see if there were any foods which triggered his eczema, but there weren't any. […] I am currently Breastfeeding DS2 and have started another food diary but so far can't pinpoint any foods which are triggers"
> — Rhu46lzq, 2011-12-15, Netmums — [link](https://www.netmums.com/coffeehouse/being-mum-794/babies-birth-12-months-58/690360-eczema-advice-please.html)

> "Well we looked into pet dander etc. (we don't have pets) and I dunno pretty inconclusive really. Everything seems inconclusive! Thinking of doing yet another food diary too."
> — Lau43jed, 2012-05-19, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/766615-please-help-eczema.html)

> "I'm trying to figure out what triggers it but honestly have no idea! […] I keep getting keep a food diary from my GP!"
> — Lau51rbt, 2015-09-01, Netmums — [link](https://www.netmums.com/coffeehouse/being-mum-794/toddlers-1-3-years-59/1362193-excema-milk.html)

> "We went down the diet route but couldn't find any patterns."
> — emm74zvl, 2011-03-15, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/548827-baby-8-months-eczema.html)

> "We've never found a trigger for him – he's bf so it could be something in my diet but we've no idea what – then again it might not be food"
> — Ela65mcy, 2008-03-11, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/153310-any-suggestions-how-deal-small-stubborn-patch-eczema.html)

> "I have been keeping a diary of what she has been eating to see if anything is triggering it off. I thought it was cheese related, but she didn't have cheese for it to flare up at the weekend."
> — 2009-03-10, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/265354-10-month-old-eczema.html)

## 2. The correlation is invisible — the strongest single quote in the harvest

> "I just can't understand why it's great one day, and then overnight it's horrific! I'm keeping a food diary and even though I'm feeding him the same things everyday, the eczema gets better and worse! I just can't see what's doing it. Can it be something as simple as heat? Or cold? […] Can you tell I'm just trying to desperately think of anything and anything?!?!?"
> — 2015-02-17, Netmums — [link](https://www.netmums.com/coffeehouse/being-mum-794/babies-birth-12-months-58/1254503-parents-eczema-babies.html) *(verified verbatim by direct re-fetch)*

> "I couldn't work out a cause (food, laundry, pet - had none! - bath products -used none...etc etc). Never did find out a cause."
> — Vsgt04pcc, 2015-02-17, Netmums, same thread

> "Even when we kept on top of the moisturising dd still had bad flare ups (with no apparent change to exposure to potential irritants)"
> — Vsgt04pcc, 2015-02-17, Netmums, same thread

> "I have noticed over the last few weeks that it can be fine for a few days and appear almost cleared and then suddenly flare up really badly. […] I'm guessing I need to keep a food diary so I can look back when she does have a reaction? But how long after eating something is she likely to react to it?"
> — amy s(11), 2015-07-15, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/1334679-eczema-food-allergy.html)

> "You would likely see a reaction within a few hours - the rash would start to develop or she would start itching - but it can take 3 days."
> — Jo 16sui, 2015-07-15, Netmums, same thread

> "The fact that they can be anything. Stress, a cold, scented candles, food, the pet cat….there is no one place to start looking and you can't possibly eliminate every possible trigger so it makes it hard to ever pin down what the triggers actually are."
> — 2026-06-21, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1ubekg0/looking_to_interview_parents_who_have_kids_with/osvkqmf/)

> "tracking triggers is really the key but it can take forever to figure them out especially with a baby who can't tell you what bothers them one thing that helped me was keeping like a really detailed log - what he ate (if he's eating solids), what products you used that day, weather changes, even things like did you change laundry detergent recently. sometimes the trigger isn't obvious at first but patterns show up after few weeks of tracking"
> — 2026-05-18, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1tgsqfx/how_long_does_a_flare_last/omj2qv9/)

> "I'm with you, I've learned to be more resilient but when I don't see any improvements I just cry. Bc I can't think about what else do I need to do to help my baby. It's so heartbreaking, I just guess and trying to figure it out every day what's the trigger."
> — 2026-06-25, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1udcice/do_you_eczema_sufferers_ever_think_about_how/otnlx46/)

> "Tracking is hard for me as well. Most times it's bit difficult to pinpoint what exactly caused a flare on my eczema areas."
> — 2026-01-29, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1qov6fy/does_anyone_else_feel_like_their_eczema_isnt/o2co5bl/)

> "this may not be helpful but my baby has chronic eczema around the face and neck and also had reactions to steroid cream so we can't use it. We have no idea what the root cause is."
> — 2025-06, r/beyondthebump — [link](https://www.reddit.com/r/beyondthebump/comments/1lggfd7/i_feel_destroyed_by_my_babys_eczema_is_there/myzg6v7/)

> "I feel it gets complicated as symptoms of the milk allergy like snotty nose and irritability and bad poos are also teething symptoms so it hard to know what's what."
> — 2020-01-02, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/1884085-milk-allergy.html)

> "However his eczema came up about 4 weeks and has just got progressively worse. He has not had any dairy and I'm so confused as to what's wrong."
> — Sho1014, 2015-06-07, HealthUnlocked MY SKIN — [link](https://healthunlocked.com/my-skin/posts/131905992/eczema-flare-up-but-dairy-free-toddler)

> "I had that one seemingly crazy week where I was pulling out every soap in our house and compari ng ingredients."
> — 2026-08-31, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1w1f7zg/biopsy/p706mbi/)

## 3. What they actually use today: paper, a notebook left at the wrong house, a shared sheet nobody updates

The single richest passage found anywhere is a grandfather's launch post in r/beyondthebump. It walks the entire tool-failure ladder in four sentences:

> "We knew something was setting it off, but figuring out what felt basically impossible. […] I should also mention that she splits time between two households, hers and ours, different food, different soaps, different everything really. **Trying to track anything across two houses is a nightmare honestly. First we tried writing it down in a notebook but kept forgetting it at one house. Then a shared Google Sheet that nobody updated consistently. We tried a shared notes app. None of it stuck and she was still scratching every night.** One night after another round of "what did she eat," "which lotion," I just looked at my wife and said I wonder if I can build an app for this."
> — sleclair, 2026-07-06, r/beyondthebump — [link](https://www.reddit.com/r/beyondthebump/comments/1up1b67/i_was_struggling_so_i_built_an_app_to_help_figure/)

> "I tried using tracker apps and they were all clumsy and annoying. I use a pen/paper and a red/yellow/green marker to just jot down notes on the day. Did we do anything new, try new foods, etc."
> — E0H1PPU5, 2026-06-21, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1ubekg0/looking_to_interview_parents_who_have_kids_with/osvkqmf/)

> "However, it's kind of difficult to keep that diary so later I moved from paper one to the app and now I'm using LittleClues app to write down my food."
> — 2026-08-04, r/FoodAllergies — [link](https://www.reddit.com/r/FoodAllergies/comments/1vevx0p/breastfeeding_and_food_allergysensitivity/p1pnwip/)

> "I kept a food diary for him but was logging at the product level; "sunflower butter and jelly sandwich, coconut milk ice cream" etc. It took me way too long to realize there was pea protein in a bunch of dairy free processed foods that was triggering his flares."
> — 2025-08-19, r/FoodAllergies — [link](https://www.reddit.com/r/FoodAllergies/comments/xarbty/finding_my_trigger/n9glrnc/)

> "i do keep a diary but im having to put everything in it like her sleeping how meany time she gets up to have a coughing fit and what her poo is like ect."
> — 2009-02-25, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/260685-please-help-possible-food-allergy.html)

> "I am keeping a food diary to show the Dermatologist when we have the appointment on 23rd December. I am also logging the creams I am using and the condition of his skin."
> — Rhu46lzq, 2008-12-08, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/breastfeeding-990/234446-breastfeeding-eczema.html)

> "I also kept a diary for about 3 weeks on everything - sleep, feeds etc. This helped as well because I have 'proof' something was up."
> — Cam62pew, 2010-10-28, Netmums — [link](https://www.netmums.com/coffeehouse/being-mum-794/babies-birth-12-months-58/488644-4-month-old-possible-dairy-allergy.html)

> "Hi candy, if you are starting a food diary, you really do have to be a detective! Check all food labels and ask nursery to save labels for you as simple things can contain milk" … "Re: food diary thanks for the advice. Didn't realise it was so indepth!!"
> — 2013-01-09, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/871230-food-allergy-kids-advice-needed-please.html)

> "Best thing you can do is make a RIGID food diary and see if you can find a pattern before you ask the HV or Doc to refer you […] Write every little thing and every poo down"
> — Ubtw18ixp, 2010-09-26, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/475373-will-dr-test-my-child-food-intolerances.html)

> "I kept a food diary for months writing reactions down and everything she ate. The dietician will ask you to do this, it really helps work out what's causing problems."
> — 2012-02-22, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/718343-i-think-our-one-year-old-boy-has-egg-allergy.html)

> "I have this fab app on my phone which tells me any dairy in product when I scan the barcode"
> — Ama61ewo, 2013-02-04, Netmums — [link](https://www.netmums.com/coffeehouse/being-mum-794/toddlers-1-3-years-59/885149-dairy-intolerance-confused-mummy.html)

**Note what is missing from this whole group.** Across the ~909-thread Netmums / patient.info / HealthUnlocked corpus there is **not one mention of an eczema or symptom-tracking app, a spreadsheet, or the Notes app.** The only software mentioned at all is a barcode label-scanner, and the only spreadsheet reference found anywhere is Reddit advice — "I recommend keeping a food diary (**can even be a spreadsheet**) to track what he consumed" ([r/FoodAllergies, 2026-08-01](https://www.reddit.com/r/FoodAllergies/comments/1vcc9du/mystery_allergy_reactions_to_boxed_mac_and_cheese/p10j7vf/)).

## 4. Photos — always evidence for a clinician, never a record the parent reviews

Every single photo mention found frames the photo as something to *show a doctor*. Not one frames it as a longitudinal record the parent goes back through to compare weeks. The one partial exception is retrospective and accidental.

> "I always take photos to share with our doc. I take a few of our best days, a few of our worst days, and a few of what I feel like our average days are. It gives her an accurate portrayal of what his life is actually looking like. Combined with the red/yellow/green journal it makes it helpful to be able to show her exactly how bad his flares are and for how long."
> — E0H1PPU5, 2026-06-21, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1ubekg0/looking_to_interview_parents_who_have_kids_with/osvkqmf/)

> "He's nearly always had 'rosy cheeks' and **looking back through photos I can see a slight redness under his cheeks as long ago as 2 years when he was 1 year old.**"
> — 2021-04-18, patient.info — [link](https://community.patient.info/t/please-help-toddler-face-rash/760239) *(verified verbatim by direct re-fetch)*

> "We took photos during this time and took them to our GP and explanied when he had/hadnt had milk."
> — 2015-09-01, Netmums — [link](https://www.netmums.com/coffeehouse/being-mum-794/toddlers-1-3-years-59/1362193-excema-milk.html)

> "Have you thought about keeping a food diary and note when the rash appears, and when is doesn't? […] Alongside this I would also take photos on your phone so you can link the photos with the rash that appeared."
> — Tracey B(344), 2014-01-29, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/1058012-rash-daughters-face-possible-food-milk-allergy.html)

> "It might be worth taking some photos of the rash to take with you in case the rash goes before the appointment."
> — Mag42hah, 2011-07-26, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/612054-phlegm-phlegm-more-phlegm-resulting-im-vomiting-baby-allergy-hayfev.html)

> "Keep a diary of her feeds, rashes and stools. Take photos. This will all help as part of her assessment too."
> — Emma M(3238), 2019-02-08, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/1836902-reflux-allergy.html)

> "i also went armed with photos of my sons skin at its worse state and the dermatoligist was actually excellent, and felt is skin!"
> — dan03ujs, 2008-11-09, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/225068-paediatric-dermatology-appointment-severe-eczema-what-should-i-expect.html)

> "so I took a photo of it on my phone and showed the doctor. When he looked into it, the only ingredient Daddies had that the other tomato sauces didn't was potassium sorbate"
> — Row80dvg, 2012-01-25, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/710284-potassium-sorbate-allergy.html)

> "Appointments are scarily short so you need to be super organised. Healthcare systems aren't always joined up and your dermatologist may not have access LOs notes, or not have had time to read them. […] If that is impractical, take photos of them (including the pharmacist sticker with the date issued and the ingredients)."
> — 2026-07-17, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1uylnpy/4_month_old_finally_seeing_a_dermatologist/oy348hu/)

## 5. Elimination diet while breastfeeding — the real burden

> "On day 3 and struggling didn't realise how many foods contained some form of dairy even plain digestives!"
> — 2017-11-23, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/breastfeeding-990/1732560-dairy-free-diet-breastfeeding.html)

> "I'm still going to cut it out as of today when we go food shopping and I really hope it helps, but breastfeeding will be so difficult from now on as all of my favourite foods have some form of dairy in"
> — Elisabeth (5), 2016-06-11, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/breastfeeding-990/1514844-bfing-possible-dairy-allergy-intolerance.html)

> "Dairy free is hard going - lots of label checking. Food that you wouldn't even consider to have milk in probably does […] I have to say that I didn't see much of a change"
> — 2015-02-24, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/breastfeeding-990/1257829-dairy-free-diet-breastfeeding.html)

> "I'd just stick to eliminating dairy first otherwise if you do both at once you won't know which one he's responded too! […] it can take up to 4 weeks to completely leave your system then a further time to leave your baby's system"
> — Ali40ssv, 2016-06-08, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/breastfeeding-990/1515219-cmp-allergy-elimination-diet.html)

> "TBH, she's still being very sick a week in to the exclusion diet, so not sure it's necessarily going to be this. Will try keeping a food diary in the meantime to see if I can draw any other conclusions."
> — 2014-11-20, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/breastfeeding-990/1203860-ebf-baby-dairy-intolerance.html)

> "It takes 6weeks for a allergen to leave breastmilk but you may find a difference in 4 to 7 days. […] I couldn't get to the bottom of my sons issues and pin point what the cause was."
> — 2020-09-24, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/1914240-multiple-food-allergies-help-please.html)

> "I did the elimination diet while I was breastfeeding and it was horrible. After my daughter was tested for her allergies, I learned I probably would have never been successful with the elimination diet because she's allergic to so many things and some were uncommon food allergies."
> — 2026-04-05, r/FoodAllergies — [link](https://www.reddit.com/r/FoodAllergies/comments/1sckvqe/elimination_for_breastfeeding/oed2ruv/)

> "I had to switch him to nutramigen bc I was doing elimination diet to determine what was bothering him. **I was down to chicken and rice. It turns out he was allergic to rice.**"
> — 2026-08-30, r/FoodAllergies — [link](https://www.reddit.com/r/FoodAllergies/comments/1w1hqya/switching_from_bf_to_nutramigen/p6pecas/)

> "I don't think most people understand extreme food elimination and it is a bitch."
> — 2026-03-11, r/FoodAllergies — [link](https://www.reddit.com/r/FoodAllergies/comments/1rqi9yt/in_need_of_a_very_particular_shake/o9sk2w9/)

> "I have had to remove all my sons trigger foods from my diet while breastfeeding. We actually first successfully identified his triggers through a food journal for me and nursing."
> — 2026-08-14, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1vnu2iy/breastfeeding_toddler_with_eczema/p3kdx8k/)

> "It took 5 months to pinpoint all the triggers for me to eliminate (dairy, egg, tree nuts, soy) but all of those came back positive when he got skin and blood tested for allergies at 1 year. […] After 5 months of unknowingly "poisoning" him, he finally was sleeping too!!"
> — 2026-08-04, r/FoodAllergies — [link](https://www.reddit.com/r/FoodAllergies/comments/1vevx0p/breastfeeding_and_food_allergysensitivity/p1ku5wm/)

## 6. Exhaustion, and no time for the method

> "i have to make a food diary for the next 6 months before they test him for anything. it is unbeliveable what he is like at bed time. […] it is so stressful for the whole family. […] i just dont know what to do anymore, we are all losing sleep over it."
> — 2012-03-05, Netmums, thread titled **"eczema ruining our lives."** — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/730580-eczema-ruining-our-lives.html)

> "I'm at my wits end now. I don't know what else to do […] my doctor wants to try a trial and error with the creams but **I don't have time for it if I'm honest!**"
> — Ecnd40jbx, 2015-10-31, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/breastfeeding-990/393841-breastfed-baby-eczema.html)

> "This morning I got up and there was blood on the baby grow were he had been scratching in the night, 4.40 this morning he was us screaming had to rock him till he went back again! […] I really don't have time for trial and error of creams."
> — Ecnd40jbx, 2015-11-01, Netmums, same thread

> "Im running out of ideas and my girlfriend is wary of any more experimenting to get results. […] Topically ive given up"
> — 2019-08-26, patient.info — [link](https://community.patient.info/t/baby-eczema/711805)

> "When she was younger I found it all too easy to get obsessed with gaining information and it's easy to feel bombarded."
> — 2009-03-16, Netmums — [link](https://www.netmums.com/coffeehouse/being-mum-794/babies-birth-12-months-58/266918-baby-eczema.html)

> "Its just so overwhelming my partner has crohns he works full time so between that and being sick he doesn't be here to do day feeds and is too tired to do nights so it's alot"
> — Lisa O(3), 2021-11-11, Netmums — [link](https://www.netmums.com/coffeehouse/drop-clinic-984/baby-child-health-989/b769f4e2-reflux-cows-milk-protein-allergy-lactose-intolerant-kidney-reflux-who-k.html)

> "I feel like I'm fighting a losing battle and am heartbroken."
> — 2025-06-20, r/beyondthebump, **59 points, 120 comments** — [link](https://www.reddit.com/r/beyondthebump/comments/1lggfd7/i_feel_destroyed_by_my_babys_eczema_is_there/)

> "I am weeping as I write this, as is my baby's horrible rash."
> — 2026-02-03, r/beyondthebump — [link](https://www.reddit.com/r/beyondthebump/comments/1qv7vjq/help_help_help_eczema/)

## 7. Memory — but the evidence for it is from newborn tracking generally, not eczema

The "I can't remember what her skin looked like last Tuesday" complaint the ticket hypothesised **was not found**. What was found is the adjacent, well-attested newborn-memory complaint — worth recording precisely because it is the nearest real thing, and it is about feeds and nappies, not skin.

> "In the first few days after birth, I used the notes app in my phone to record feeds/nappies etc, mainly as I was so tired I couldn't remember otherwise!"
> — 2026-08, r/NewParents — [link](https://www.reddit.com/r/NewParents/comments/1vz1b18/who_is_using_newborn_tracking_apps_why_or_why_not/p6duk1j/)

> "I was lucky to remember to brush my teeth, let alone how many diapers I was changing in those first weeks."
> — 2026-08, r/NewParents — [link](https://www.reddit.com/r/NewParents/comments/1vz1b18/who_is_using_newborn_tracking_apps_why_or_why_not/p62fhd3/)

> "I realized I couldn't actually remember exactly when the last feed/nap/diaper was without tracking it somewhere."
> — 2026-08, r/NewParents — [link](https://www.reddit.com/r/NewParents/comments/1vz1b18/who_is_using_newborn_tracking_apps_why_or_why_not/p6277u9/)

> "I'm about two weeks post partum (FTM) and just have been using the notes app on my phone and setting alarms for every three hours for feeds."
> — 2026-08, r/NewParents — [link](https://www.reddit.com/r/NewParents/comments/1vz1b18/who_is_using_newborn_tracking_apps_why_or_why_not/p67fi9q/)

> "I am prone to anxiety and an app would just make that worse."
> — 2026-08, r/NewParents — [link](https://www.reddit.com/r/NewParents/comments/1vz1b18/who_is_using_newborn_tracking_apps_why_or_why_not/p68c44i/)

The eczema-specific version of the memory complaint appears once, and only as self-description:

> "I think the best we can do is continue tracking triggers (and for me, be more meticulous since I am forgetful - that Lemma Health app will help with this at least) and be strict about each treatment we test to see if it is actually working."
> — 2026-06-02, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1tv68fr/eczema_around_mouth_what_were_your_triggers/opf3gvh/)

## 8. Records as leverage on a healthcare system that will not move

Not a complaint about tracking — a *use* for it, and the only one anybody reports paying off. Worth its own group because it suggests where the value actually is.

> "It took us 11 years of tracking and allergy testing, lifestyle and diet changes and **my record keeping** to get Dupixant."
> — 2026-04-27, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1swohu0/looking_for_recommendations/oih7mnu/)

> "Often the doctors don't understand the food connections with eczema so you might need to look for the links yourself."
> — 2026-09-04, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1w6pqqc/baby_eczema/p7puy17/)

> "Be aware that the dermatologist's first priority will be to heal your LOs skin, not to track down triggers."
> — 2026-07-17, r/eczema — [link](https://www.reddit.com/r/eczema/comments/1uylnpy/4_month_old_finally_seeing_a_dermatologist/oy348hu/)

## 9. Existing-app complaints

Thin, because almost nobody uses one. Everything found:

> "I tried using tracker apps and they were all clumsy and annoying."
> — r/eczema, 2026-06-21 — [link](https://www.reddit.com/r/eczema/comments/1ubekg0/looking_to_interview_parents_who_have_kids_with/osvkqmf/)

> "App works well and is pretty straightforward. It's a little annoying that it asks to save portions of information rather than does so automatically. I would also appreciate a push notification option for reminders to track at some point in the day."
> — EczemaWise review, Google Play — [link](https://play.google.com/store/apps/details?id=com.eczemawiseapp&hl=en_US)

> "Deleted after seeing the drop down menu options for selecting my child's gender. Their options are non-scientific and undermine any confidence I would have in the kind of help or advice his app would give me."
> — EczemaWise review, Google Play — [link](https://play.google.com/store/apps/details?id=com.eczemawiseapp&hl=en_US)

NEA's own replies on that listing show the recurring failure mode was **registration friction and crashes**, e.g. "Hello Benedict, we're sorry you deleted the app after seeing our registration process" and "we aim to provide you with a personalized experience and effective free tool to manage your eczema, which is why we ask a few questions at registration."

---

## What this does to the premise

**Confirmed.** The audience is real, reachable and in visible distress; r/eczema, r/beyondthebump and the Netmums allergy/eczema boards produce fresh threads continuously, and the emotional register is extreme ("I feel destroyed", "I am weeping as I write this", "eczema ruining our lives"). The elimination-diet-while-breastfeeding cohort — exactly the target ICP — is well populated and articulate.

**Weakened, in three specific ways.**

1. **The problem statement is one step off.** Parents do not complain that logging is hard. They complain that **the log produces no answer** — because eczema lags, has non-food triggers, and confounds with teething and weather. A better diary does not fix that. Ten of the strongest quotes in this file are a parent who *did* keep the diary, correctly, and got nothing. A product whose promise is "log it more conveniently" is answering a question nobody asked; a product whose promise is "make sense of what you logged" is answering the real one, and that is a much harder claim to make honestly.
2. **The incumbent is exiting, and its numbers say why.** NEA — the largest US eczema charity, 66,250 Facebook followers — built exactly this app, gave it away free, and is **shutting it down on 2026-12-18** having reached 5K+ Android downloads. That is either a large opening or a demonstrated ceiling, and this research cannot distinguish them.
3. **Distribution is worse than it looks.** Every UK charity venue is relationship-gated rather than postable. Facebook group sizes and all TikTok counts are unverifiable without a logged-in human. And on Reddit, the two people who ran this exact play in 2026 — one recruiting parents, one launching a trigger-tracking app — scored **1 point and 3 comments between them**, unmoderated. Permission is not the constraint. Attention is.

**One thing worth noticing on the other side.** Photos in this corpus are *always* clinician-facing and *always* reactive — taken because the rash might be gone by the appointment. The single retrospective use found ("looking back through photos I can see a slight redness … as long ago as 2 years") was accidental, and it worked. Nobody is deliberately building a visual record. Whether that is an unmet need or an unwanted one is not answerable from this evidence, and would need interviews.

## Open questions this could not close

- **Facebook group sizes and rules.** Needs a logged-in human. Four named groups are listed above as starting points.
- **TikTok hashtag volume.** Needs a logged-in human on a non-proxied network.
- **Current Reddit subscriber counts and the actual text of each subreddit's self-promotion rule.** Needs a human with a browser, or Reddit API credentials. Ten minutes of work; do not let the 2025-02 snapshot figures leak into anything external before then.
- **Whether the Mumsnet £30 lane converts.** The rule and the price are verified from Mumsnet's own Netiquette page; what a £30 Non-member-requests post actually yields in replies is not, and would need one £30 experiment to find out. That is the cheapest single test in this whole file.
- **Whether "make sense of the log" is a promise anyone would pay for.** This corpus can prove the failure of the diary. It cannot prove appetite for the fix. That is an interview question, and there is a warm lead: two people were openly recruiting eczema parents for exactly these interviews on Reddit in mid-2026.
