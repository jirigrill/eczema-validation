# What conversion rate on a pre-launch landing page actually constitutes a signal

Research findings for [#5](https://github.com/jirigrill/eczema-validation/issues/5). Inputs only — **this file deliberately does not propose the pass/fail bar.** That belongs to [#7](https://github.com/jirigrill/eczema-validation/issues/7).

Every row below is tagged `[primary]` (read on the publishing organisation's own page) or `[secondhand]` (quoted by someone else; original unreachable). Where a widely-repeated figure traces to nothing, that is recorded as a finding, not silently dropped.

---

## 0. The headline, before the tables

**There is no published dataset measuring visitor→email conversion on pre-launch waitlist pages, broken out by traffic source.** Every waitlist-specific number in circulation comes from a waitlist-tool vendor's blog with no disclosed dataset. One of those vendors ([Waitlister](https://waitlister.me/growth-hub/blog/waitlist-and-product-launch-statistics)) says so about its own field in the same article it publishes numbers in: *"the waitlist world has been largely opaque"* and *"most numbers floating around the internet are either misleading or completely made up."* `[primary — a vendor's own admission]`

What *does* exist, with real methodology behind it, is landing-page conversion for **live products** — split by channel, at large N. Those are the defensible anchors. They measure a different funnel and are lower-bound-ish analogues, not substitutes.

---

## 1. Benchmark table — general landing pages, by traffic source

| Rate | Traffic source | Source & dataset | Tag |
|---|---|---|---|
| **6.6%** median, all industries | Mixed (paid + organic landing-page traffic) | [Unbounce Conversion Benchmark Report](https://unbounce.com/conversion-benchmark-report/) — 41,000+ landing pages, 464M visitors, 57M+ conversions | `[primary]` |
| **5.1%** median, Healthcare/Wellness/Medical | Mixed | [Unbounce — Healthcare, Wellness & Medical](https://unbounce.com/conversion-benchmark-report/healthcare-wellness-conversion-rate/). Sub-splits: Wellness 8.2%, Medical Treatment 5.3%, Dental 4.3% | `[primary]` |
| **3.8%** median, SaaS (75th pct 11.6%) | Mixed | [Unbounce — industry table](https://unbounce.com/landing-pages/whats-a-good-conversion-rate/) | `[primary]` |
| **16.9%** | **Email** | [Unbounce — SaaS by channel](https://unbounce.com/conversion-benchmark-report/saas-conversion-rate/) | `[primary]` |
| **9.2%** | **Paid social — Instagram** | Unbounce, same page | `[primary]` |
| **5.1%** | **Paid search — Google** | Unbounce, same page | `[primary]` |
| **3.5%** | **Paid social — Facebook** | Unbounce, same page | `[primary]` |
| **1.9%** | **Paid search — Bing** | Unbounce, same page | `[primary]` |
| **5.4%** | **Paid search** | [Ruler Analytics Conversion Benchmark Report 2026](https://www.ruleranalytics.com/blog/insight/conversion-rate-by-industry/) — 110M+ sessions, 5M+ conversions, 13 industries, £33.8M tracked spend, multi-touch attribution | `[primary]` |
| **4.9%** | **Organic search** | Ruler Analytics, same report | `[primary]` |
| **4.9%** | **Email** | Ruler Analytics, same report | `[primary]` |
| **4.8%** | **Referral** | Ruler Analytics, same report | `[primary]` |
| **4.7%** | **Direct** | Ruler Analytics, same report | `[primary]` |
| **2.23%** | **Organic social** | Ruler Analytics, same report | `[primary]` |
| **2.11%** | **Paid social** | Ruler Analytics, same report | `[primary]` |
| **7.52%** overall; Physicians & Surgeons 11.62%, Dentists 9.08% | Google Search ads (ad-click→conversion) | [WordStream/LOCALiQ Google Ads Benchmarks 2025](https://www.wordstream.com/blog/2025-google-ads-benchmarks) — 16,446 US search campaigns, Apr 2024–Mar 2025, min. 64 campaigns per category | `[primary]` |
| **7.72%** overall lead-gen; Health & Fitness 5.63% (CPL $52.98) | Facebook/Instagram ads (ad-click→lead form) | [LOCALiQ Facebook Advertising Benchmarks 2025](https://localiq.com/blog/facebook-advertising-benchmarks/), updated Oct 2025 | `[primary]` |

### Reading notes on the above

- **Unbounce reports the median deliberately**, and says why on its own page: *"Averages are susceptible to skewing when extreme outliers exist on either end of the spectrum."* Any benchmark quoted as an "average" is a different and usually higher statistic.
- **Unbounce and Ruler disagree on paid social by 4x** (Instagram 9.2% vs paid social 2.11%). They are not measuring the same thing: Unbounce counts a landing-page goal completion, Ruler counts a *qualified lead or sale* under multi-touch attribution. Ruler's definition is further down the funnel and therefore lower. Neither is wrong; the gap is the definition.
- **WordStream and LOCALiQ measure ad-click→conversion, not landing-page-visitor→conversion.** Different denominator (the ad platform's click count, not page sessions) and different numerator (a tracked conversion action). They are a sanity check on order of magnitude, not a like-for-like input.
- WordStream labels its figure "average" in the headline while describing it in-report as outlier-adjusted. Their own labelling is inconsistent; treat the number as median-ish.
- **Unbounce has no "Family & Community", "Parenting" or "Baby" category.** Healthcare/Wellness/Medical at 5.1% is the nearest thing that exists.

---

## 2. Waitlist-specific figures — all of them unsourced

Recorded so nobody re-derives them later and mistakes them for data.

| Claim | Where it comes from | Dataset disclosed? |
|---|---|---|
| SaaS waitlists 3.4%, AI tools 4.6%, consumer apps 4.1%, "8–9%+ = top tier" | [LaunchList Waitlist Benchmark](https://getlaunchlist.com/tools/waitlist-benchmark), which attributes to "First Round Capital's pre-launch dataset, OpenView SaaS benchmarks, aggregated Product Hunt reporting" | **No.** None of the three named sources could be located publishing anything of the kind. Treat the attribution chain as unverifiable. |
| Warm traffic 15–35%, community (IndieHackers/HN/Reddit) 8–15%, cold paid 3–8% | [LaunchList FAQ](https://getlaunchlist.com/help/faq/strategy-growth) — self-described "rough industry benchmarks" | No |
| Organic 25–35% vs paid 10–20% | [CraftUp blog](https://craftuplearn.com/blog/waitlist-landing-page-anatomy-incentives-benchmarks) | No |
| "Average waitlist ≈15%, good 20–30%, top 40–85%" | [Waitlister](https://waitlister.me/growth-hub/blog/waitlist-and-product-launch-statistics) | No — and the same article says the numbers in the field are "completely made up" |

**Every one of these is published by a company that sells waitlist software.** The direction of the incentive is worth stating plainly: a vendor whose product is a signup form benefits from signups looking easy.

The only first-hand waitlist/pre-launch numbers found are N=1 founder anecdotes, useful as existence proofs and nothing else: [60 of the first 100 customers from one Reddit post, $0 spend](https://www.indiehackers.com/post/how-i-got-my-first-60-customers-from-reddit-without-spending-a-dime-on-ads-3d19b2c47c); and a separate founder reporting [$500 of Meta ads → 2 signups, $200 of Reddit ads → 0](https://www.indiehackers.com/product/excelly-ai/reddit-ads-experiment-how-much-we-paid-for-100-clicks--NNi-kbdzmeulsgLFnqO). The spread between those two outcomes is the actual finding.

---

## 3. Folklore audit — figures that trace to nothing

| Claim | Where the trail ends | Verdict |
|---|---|---|
| **"15–20% visitor→email for a waitlist page"** — the number this ticket exists to replace | Traced through getlaunchlist, waitlister, kickofflabs, flowjam, craftup. All waitlist-tool vendors, all citing each other or nobody. | **Dies at circular vendor assertion. No dataset anywhere.** |
| **"A good landing page converts at 10%"** | Popularised by Unbounce's older marketing copy. Unbounce's own 57M-conversion report puts the all-industry median at 6.6% and SaaS at 3.8%. | **Misrepresents its own apparent origin.** 10% is top-quartile, not "good baseline". |
| **"Average email opt-in rate is 1.95%"** / **"Sumo analysed 1.7bn popups: 3.09% average, 9.28% top decile"** | Ubiquitous across CRO blogs. Every path terminates at a *retrospective mention* in [BDOW's own blog](https://bdow.com/stories/pop-up-statistics/) ("since 2016, when Sumo analyzed 1.75 billion pop-ups") with **no link to the original**. Sumo rebranded to BDOW; the original post is unreachable and was not recoverable via search. | **Dead trail. Do not cite as data.** |
| **HubSpot "23% average landing page conversion"** and the "186,000 businesses A/B testing" stat | Appear only in third-party aggregator blogs. Could not be located on hubspot.com or in the State of Marketing report itself. | **Unverifiable. Possibly fabricated by a citing blog.** |
| **"You need 100 signups to validate"** | Repeated across generic startup-validation blogs. No consistent named source, no study, ever. | **No origin at all — a round number that stuck.** |
| **Sean Ellis 40% "very disappointed" PMF test** | Real and named: [Sean Ellis, startup-marketing.com](https://www.startup-marketing.com/deconstructing-startup-growth/), c. 2009–2010, from his own work across Dropbox/LogMeIn/Eventbrite/Lookout, claiming he benchmarked "almost 100 startups". | **Genuine first-hand practitioner observation, but he never published the startups, verticals, geography or raw numbers.** Directional, not calibrated. Also measures existing users, not pre-launch visitors — see §6. |
| **"Bounce probability rises 32% as load goes 1s→3s"** | Attributed to a 2016 Google/SOASTA mobile speed study of ~900k landing pages. The original Google URL did not resolve. | `[secondhand]` — plausible, widely repeated, primary not confirmed. Use only as a directional reason to keep the page fast. |

---

## 4. How many visitors before a rate means anything

### 4.1 Method, and why the obvious one is wrong

The normal-approximation (**Wald**) interval `p̂ ± z√(p̂(1−p̂)/n)` is the one most calculators use and it is the wrong tool here. It produces bounds below 0%, and its true coverage oscillates erratically and sits well below the nominal 95% **even when the textbook `np > 5` / `np(1−p) > 10` rule is satisfied** — the rule of thumb is itself defective.

> Brown, Cai & DasGupta (2001), *Interval Estimation for a Binomial Proportion*, **Statistical Science 16(2):101–133** — open access at [Project Euclid](https://projecteuclid.org/journals/statistical-science/volume-16/issue-2/Interval-Estimation-for-a-Binomial-Proportion/10.1214/ss/1009213286.full). Recommends the **Wilson score** or **Jeffreys** interval instead. `[primary]`

> Agresti & Coull (1998), *Approximate is better than exact for interval estimation of binomial proportions*, **The American Statistician 52(2):119–126** — [publisher](https://www.tandfonline.com/doi/abs/10.1080/00031305.1998.10480550), [full text mirror](https://math.unm.edu/~james/Agresti1998.pdf). Exact (Clopper–Pearson) is needlessly wide, Wald is anti-conservative; Wilson tracks nominal coverage at small n. `[primary via mirror]`

**Use the Wilson score interval.** Every figure in §4.2 was computed directly, not quoted.

### 4.2 Wilson 95% intervals at plausible sample sizes

| n | signups k | point est. | Wilson 95% CI | CI width (pp) |
|---|---|---|---|---|
| 100 | 0 | 0.0% | 0.0% – 3.7% | 3.7 |
| 100 | 1 | 1.0% | 0.2% – 5.4% | 5.3 |
| 100 | 2 | 2.0% | 0.6% – 7.0% | 6.5 |
| 100 | 5 | 5.0% | 2.2% – 11.2% | 9.0 |
| 100 | 10 | 10.0% | 5.5% – 17.4% | 11.9 |
| 100 | 15 | 15.0% | 9.3% – 23.3% | 14.0 |
| 100 | 20 | 20.0% | 13.3% – 28.9% | 15.5 |
| 200 | 2 | 1.0% | 0.3% – 3.6% | 3.3 |
| 200 | 4 | 2.0% | 0.8% – 5.0% | 4.2 |
| 200 | 10 | 5.0% | 2.7% – 9.0% | 6.2 |
| 200 | 20 | 10.0% | 6.6% – 14.9% | 8.4 |
| 200 | 30 | 15.0% | 10.7% – 20.6% | 9.9 |
| 300 | 3 | 1.0% | 0.3% – 2.9% | 2.6 |
| 300 | 6 | 2.0% | 0.9% – 4.3% | 3.4 |
| 300 | 15 | 5.0% | 3.1% – 8.1% | 5.0 |
| 300 | 30 | 10.0% | 7.1% – 13.9% | 6.8 |
| 300 | 45 | 15.0% | 11.4% – 19.5% | 8.1 |
| 500 | 5 | 1.0% | 0.4% – 2.3% | 1.9 |
| 500 | 10 | 2.0% | 1.1% – 3.6% | 2.6 |
| 500 | 25 | 5.0% | 3.4% – 7.3% | 3.9 |
| 500 | 50 | 10.0% | 7.7% – 12.9% | 5.3 |
| 500 | 75 | 15.0% | 12.1% – 18.4% | 6.3 |

Read the third row group: **10 signups from 100 visitors is not "a 10% conversion rate."** It is consistent with anything from 5.5% to 17.4%. That single interval straddles Unbounce's healthcare median (5.1%), its all-industry median (6.6%), and the folklore "10% is good" line simultaneously.

### 4.3 Zero signups is much weaker evidence than it feels

The **rule of three**: with n trials and zero events, the 95% upper bound on the true rate is approximately `3/n`.

> Hanley & Lippman-Hand (1983), *If nothing goes wrong, is everything all right?*, **JAMA 249(13):1743–1745** — [full text](https://jhanley.biostat.mcgill.ca/c607/ch08/zero_numerator.pdf). `[primary via author's own course mirror; JAMA's page is paywalled]`

| Outcome | Rule-of-three upper bound | Exact Wilson upper bound |
|---|---|---|
| 0 / 50 | 6.00% | 7.13% |
| 0 / 100 | 3.00% | 3.70% |
| 0 / 150 | 2.00% | 2.50% |
| 0 / 200 | 1.50% | 1.88% |
| 0 / 300 | 1.00% | 1.26% |
| 0 / 500 | 0.60% | 0.76% |

**Zero signups from 100 visitors does not establish that the rate is near zero** — it is still consistent with a true rate of up to ~3.7%, which is inside Unbounce's SaaS median band. Only at n ≈ 300+ does a zero become a genuinely damning result.

### 4.4 Sample size to *estimate* the rate to a stated precision

`n = z²·p(1−p)/e²`, z = 1.96:

| True rate assumed | ±5pp | ±3pp | ±2pp |
|---|---|---|---|
| 5% | 73 | 203 | 457 |
| 10% | 139 | **385** | 865 |
| 20% | 246 | 683 | 1,537 |

### 4.5 Sample size to *decide against a pre-committed threshold* — much cheaper

This is the crucial asymmetry. Answering *"what is my conversion rate?"* needs hundreds of visitors. Answering *"is my rate above X or below Y?"*, when X and Y are far apart and fixed **in advance**, needs far fewer. One-sample test against a fixed p₀, α = 0.05, 80% power:

| Hypothesis | n (one-sided) | n (two-sided) |
|---|---|---|
| 5% vs 20% | 22 | 26 |
| 3% vs 10% | 58 | 71 |
| **5% vs 15%** | **44** | **53** |
| 10% vs 20% | 69 | 86 |
| 5% vs 10% | 150 | 185 |
| 2% vs 5% | 191 | 233 |

Note the last two rows: as the two rates get closer, the required n explodes. **A bar that tries to distinguish 5% from 10% is out of reach at this budget; a bar that distinguishes 5% from 15% is not.** (Input for #7 — not a recommendation.)

### 4.6 On "minimum conversions" rules

Guidance of the form "you need N conversions" comes almost entirely from A/B-testing tooling and does not transfer to estimating one page's rate:

| Source | Guidance | Note |
|---|---|---|
| [Google Ads Smart Bidding](https://support.google.com/google-ads/answer/10285843) | ~15 conversions / 30 days minimum for Target ROAS; ~30/mo for stability | This is a *bidding-algorithm training* threshold, not a statistical-significance one |
| [Google/DV360 Conversion Lift](https://support.google.com/displayvideo/answer/16804790) | ≥3,000 conversions for significant lift measurement | Two-arm experiment |
| [Optimizely sample size calculator](https://www.optimizely.com/sample-size-calculator/) | No fixed minimum; n = f(baseline, MDE, power) | Two-variant |
| VWO sample size docs | Same approach; worked example needs ~14.7k/variant (Bayesian), ~40.5k (Frequentist) | Two-variant |
| [Evan Miller](https://www.evanmiller.org/ab-testing/sample-size.html) | Requires baseline + MDE + α/power; no universal rule | Two-variant |

**None of these is the right lens for a single landing page.** Wilson interval width (§4.2) and threshold power (§4.5) are.

---

## 5. What $100–150 actually buys

Channel selection and ad-policy feasibility belong to [#6](https://github.com/jirigrill/eczema-validation/issues/6); this section exists only to make the sample-size arithmetic concrete.

| Scenario | CPC | Clicks @ $100 | Clicks @ $150 | Source |
|---|---|---|---|---|
| Meta, traffic objective, overall | $0.70 | 143 | 214 | [LOCALiQ Facebook Benchmarks 2025](https://localiq.com/blog/facebook-advertising-benchmarks/) `[primary]` |
| Meta, traffic objective, Health & Fitness | $0.80 | 125 | 187 | same |
| Meta, lead objective, Health & Fitness | $2.64 | 37 | 56 | same |
| Google Search, Health & Fitness | $6.17 | 16 | 24 | [WordStream Google Ads Benchmarks 2026](https://www.wordstream.com/blog/2026-google-ads-benchmarks) `[secondhand — aggregator panel, not Google]` |

Meta's **Health & Wellness vertical carries the highest CPM of any vertical at $20.70** per the same LOCALiQ dataset.

Two adjustments that push the real number down:

1. **Clicks ≠ landing-page visitors.** Some fraction abandon before the page renders or before analytics fires. Budget for a loss; the commonly-cited page-speed bounce figures are `[secondhand]` (see §3) so no specific discount is defensible here.
2. **Meta health-targeting restrictions may raise the cost further.** Meta's own [Health & Wellness ad standards](https://transparency.meta.com/policies/ad-standards/restricted-goods-services/health-wellness/) and [Personal Attributes policy](https://transparency.meta.com/policies/ad-standards/objectionable-content/privacy-violations-personal-attributes/) `[primary]` prohibit copy implying knowledge of a viewer's health condition — "does your baby have eczema?" is precisely the prohibited shape. Reclassification into a Special Ad Category strips targeting controls and typically raises effective CPC. This is #6's ticket, flagged here because it moves the visitor count.

**Range: roughly 16 to 214 visitors.** Only the cheapest Meta traffic-objective scenario reaches three figures.

---

## 6. Benchmarks that are NOT transferable to this situation

Stated explicitly, because the temptation to reach for each of these is real.

1. **Every waitlist-vendor figure (§2).** No disclosed dataset, published by parties selling signup forms, and one of them says in print that the field's numbers are made up. These are not benchmarks. They are marketing.

2. **All the Unbounce, Ruler, WordStream and LOCALiQ figures measure live products, not pre-launch pages.** A visitor converting there is buying, booking, or requesting a demo of something that exists. A pre-launch page asks for an email against a promise. The funnels differ in both intent and friction, in opposite directions — lower commitment (just an email) pushes the rate up, no product to evaluate pushes it down. **The net direction is unknown and unsourced.** Do not assume a pre-launch page is "obviously easier."

3. **Unbounce's "Healthcare, Wellness & Medical" 5.1% is not a parenting benchmark.** Its sub-splits (Wellness, Medical Treatment, Dental) are clinics and treatment providers buying local intent traffic. There is no baby/parenting category in any dataset found.

4. **WordStream and LOCALiQ denominators are ad clicks, not page sessions**, and their numerators are platform-tracked conversion actions, not email signups. Order-of-magnitude sanity check only.

5. **Ruler Analytics counts qualified leads and sales under multi-touch attribution** — deeper in the funnel than an email capture, and attributed across touchpoints rather than to the last click. Its channel *ordering* (paid search > organic > organic social > paid social) is the transferable part; its absolute levels are not.

6. **Unbounce's channel splits are SaaS-vertical.** Applying its Instagram 9.2% to a cold consumer parenting ad is not supported by the source.

7. **The Sean Ellis 40% PMF test cannot be run here at all.** It surveys people already *using* the product about how they'd feel if it disappeared. There is no product and no users. It has nothing to say about a landing page.

8. **A/B-test sample size guidance (§4.6) is answering a different question.** Two-arm experiments with a minimum detectable effect. There is one arm here.

9. **US and UK are pooled in most of these datasets or are US-only.** WordStream/LOCALiQ are US ad accounts; Unbounce and Ruler do not break out geography in the pages consulted. A US/UK mixed-geography test is not what any of them measured.

10. **Organic community posting has no benchmark in any of these datasets.** Ruler's "organic social" 2.11% is brand-page social traffic, not a founder posting in a parenting forum. The only evidence found for the latter is a single founder anecdote (§2) and its counterexample. If the plan includes community posting, **its conversion rate must be measured separately from paid, not blended** — blending a warm and a cold channel into one rate produces a number that describes neither and depends entirely on the mix.

---

## 7. Inputs handed to #7, in one place

- No sourced waitlist benchmark exists; the "15–20%" figure this ticket was opened to replace traces to nothing.
- Nearest defensible anchors: Unbounce all-industry median **6.6%**, Healthcare/Wellness/Medical **5.1%**, SaaS **3.8%** — all live-product, all mixed-traffic.
- Channel ordering is consistently reproduced across two independent large datasets: **email > paid search ≈ organic search ≈ direct ≈ referral > organic social ≈ paid social.** Cold paid social is the worst-converting channel in Ruler's data at **2.11%**.
- $100–150 buys **~16–214 visitors** depending on channel; realistically ~120–210 only on Meta's cheapest traffic objective.
- At n = 150, a 95% Wilson interval on a 10% observed rate is roughly **±6pp**. Estimating the rate precisely is out of budget.
- **Deciding against a pre-committed, widely-separated threshold is in budget**: 5% vs 15% needs n ≈ 44–53; 5% vs 10% needs n ≈ 150–185 and is marginal.
- **The bar must therefore be a threshold decision, not a point estimate, and the two rates it separates must be far apart.** Setting it after seeing the result forfeits even that.

---

## Sources

Unbounce: [Conversion Benchmark Report](https://unbounce.com/conversion-benchmark-report/) · [average conversion rates FAQ](https://unbounce.com/average-conversion-rates-landing-pages/) · [industry table](https://unbounce.com/landing-pages/whats-a-good-conversion-rate/) · [Healthcare/Wellness/Medical](https://unbounce.com/conversion-benchmark-report/healthcare-wellness-conversion-rate/) · [SaaS by channel](https://unbounce.com/conversion-benchmark-report/saas-conversion-rate/)
Ruler Analytics: [Conversion Rate Benchmarks 2026](https://www.ruleranalytics.com/blog/insight/conversion-rate-by-industry/)
WordStream / LOCALiQ: [Google Ads Benchmarks 2025](https://www.wordstream.com/blog/2025-google-ads-benchmarks) · [Google Ads Benchmarks 2026](https://www.wordstream.com/blog/2026-google-ads-benchmarks) · [Facebook Advertising Benchmarks 2025](https://localiq.com/blog/facebook-advertising-benchmarks/)
Meta: [Health & Wellness ad standards](https://transparency.meta.com/policies/ad-standards/restricted-goods-services/health-wellness/) · [Personal Attributes policy](https://transparency.meta.com/policies/ad-standards/objectionable-content/privacy-violations-personal-attributes/)
Statistics: [Brown, Cai & DasGupta 2001](https://projecteuclid.org/journals/statistical-science/volume-16/issue-2/Interval-Estimation-for-a-Binomial-Proportion/10.1214/ss/1009213286.full) · [Agresti & Coull 1998](https://math.unm.edu/~james/Agresti1998.pdf) · [Hanley & Lippman-Hand 1983](https://jhanley.biostat.mcgill.ca/c607/ch08/zero_numerator.pdf) · [Google Ads Smart Bidding](https://support.google.com/google-ads/answer/10285843) · [Evan Miller sample size](https://www.evanmiller.org/ab-testing/sample-size.html)
Unsourced / dead trails, recorded as such: [LaunchList benchmark tool](https://getlaunchlist.com/tools/waitlist-benchmark) · [LaunchList FAQ](https://getlaunchlist.com/help/faq/strategy-growth) · [Waitlister](https://waitlister.me/growth-hub/blog/waitlist-and-product-launch-statistics) · [CraftUp](https://craftuplearn.com/blog/waitlist-landing-page-anatomy-incentives-benchmarks) · [BDOW pop-up statistics](https://bdow.com/stories/pop-up-statistics/) · [Sean Ellis](https://www.startup-marketing.com/deconstructing-startup-growth/)
N=1 anecdotes, not benchmarks: [Reddit → 60 customers](https://www.indiehackers.com/post/how-i-got-my-first-60-customers-from-reddit-without-spending-a-dime-on-ads-3d19b2c47c) · [Reddit/Meta ads experiment](https://www.indiehackers.com/product/excelly-ai/reddit-ads-experiment-how-much-we-paid-for-100-clicks--NNi-kbdzmeulsgLFnqO)

All Wilson intervals, rule-of-three bounds, margin-of-error and power figures in §4 were computed for this document, not quoted.
