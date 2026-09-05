# Search demand and traffic cost: eczema food-trigger tracking (US + UK)

Resolves [#4](https://github.com/jirigrill/eczema-validation/issues/4). All figures accessed **2026-09-05**. Every number below names the tool that produced it. Where a number could not be obtained from a free source, that is stated rather than estimated.

## Headline

The **condition** is searched heavily; the **food-trigger tracking behaviour** is not searched at all in any measurable volume. On one normalized Google Trends scale (single request, four series, 5-year weekly, run 2026-09-05), `baby eczema` averages **40.4** (US) and **45.8** (GB) while `eczema food triggers` averages **0.03** (US) and **0.05** (GB) — roughly **three orders of magnitude** smaller. `eczema food diary app` and `eczema trigger tracker` return a flat **0** across five years in both countries.

The budget consequence is arithmetic, not judgement: at the WordStream 2026 all-industry Google Ads CPC of **$5.42**, **$150 buys ~27 clicks**. That is not enough clicks to measure a landing-page conversion rate at any useful confidence — and the keywords that would carry the intent have no impression volume to spend it on anyway. A paid **search** test is not viable in this niche. A paid **social** test is: WordStream's Facebook traffic-campaign CPC of **$0.70** all-industry / **$0.80** Health & Fitness puts $150 at **~190–215 clicks**.

## Method and its limits — read before using the table

**What I could run first-hand:**

| Tool | How | What it yields |
|---|---|---|
| Google Trends API (`trends.google.com/trends/api/explore` + `/widgetdata/multiline`, `/relatedsearches`) | called directly, `hl=en-US`, `tz=0`, `time=today 5-y`, `geo=US` and `geo=GB` | *relative* search interest (0–100 index), seasonality, related queries |
| Google Suggest (`suggestqueries.google.com/complete/search?client=firefox`) | called directly | which phrasings exist as real queries; long tail |
| WordStream / LocaliQ published benchmark reports | WebFetch of the primary pages | CPC / CPL by industry |
| Bing SERP HTML (`bing.com/search`) | called directly, `cc=US` | count of ad slots served on the niche queries |
| Wikimedia Pageviews REST API | called directly | absolute magnitude anchor for the condition (global, all-country) |

**What I could not get, and why it matters.** No free tool reachable without an account would return **absolute per-keyword monthly volume or per-keyword CPC**. Attempted and failed on 2026-09-05: Ahrefs Free Keyword Generator (JS app, no open endpoint in its `KeywordGeneratorIndex` bundle; gated), Semrush free keyword tools (login), Ubersuggest API (`app.neilpatel.com/api/keyword_info` → `401 INVALID_TOKEN`), Keyword Surfer (`db2.keywordsur.fr/keyword_surfer_keywords` → `404`, endpoint retired), SpyFu keyword overview (data loaded by authenticated XHR; `NsaApi` guesses return the SPA shell), WordStream Free Keyword Tool (SPA, no reachable API; legacy `tools.wordstream.com/fkt` serves the Performance Grader shell), SE Ranking free volume checker (no open endpoint on page), Keywords Everywhere free checker (reCAPTCHA), searchvolume.io (email-gated), searchvector.io (Next.js, no guessable route — six paths tried, all 404). Google Keyword Planner itself needs a Google Ads account.

So the **US volume / UK volume columns below are Google Trends relative indices, not monthly search counts.** They are internally comparable within the marked batch and nothing more. Anyone wanting absolute counts should paste the keyword list from this file into Google Keyword Planner (free, no ad spend required, ~5 minutes) or Ahrefs Webmaster Tools; that is the cheapest way to close the gap and it needs a human with an account.

Two further caveats:

- **Google Suggest ignored `gl=uk`.** US and UK sweeps returned byte-identical suggestion lists, so the completions below are US-IP results and cannot be read as UK-specific. Trends `geo=GB` is unaffected and is the UK evidence.
- **Google Trends normalizes per region**, so a US-vs-GB comparison is relative popularity within each country's total search volume, not a count ratio.

## Keyword table

Index columns are Google Trends 5-year weekly mean of the 0–100 index (`max` in brackets where the mean rounds to 0 but the term did register at least once). Batch letters mark which single request a set of numbers is comparable within — **do not compare across batches.**

| Term | US index | UK index | CPC estimate | Source tool | Batch | Accessed |
|---|---|---|---|---|---|---|
| `baby eczema` | **40.4** | **45.8** | n/a | Google Trends API | X (cross-geo) | 2026-09-05 |
| `eczema food triggers` | **0.03** (max 1) | **0.05** (max 6) | n/a | Google Trends API | X (cross-geo) | 2026-09-05 |
| `baby eczema` | 40.4 | 58.1 | n/a | Google Trends API | A | 2026-09-05 |
| `food diary` | 9.5 | 28.4 | n/a | Google Trends API | A | 2026-09-05 |
| `eczema food` | 6.9 | 9.2 | n/a | Google Trends API | A | 2026-09-05 |
| `eczema diet` | 3.6 | 4.2 | n/a | Google Trends API | A | 2026-09-05 |
| `eczema app` | 1.7 | 1.0 | n/a | Google Trends API | A | 2026-09-05 |
| `eczema food diary` | **0** | 0 (max 6) | n/a | Google Trends API | B | 2026-09-05 |
| `baby eczema food triggers` | 0 (max 1) | 0 (max 8) | n/a | Google Trends API | B | 2026-09-05 |
| `breastfeeding diet eczema` | **0** | **0** | n/a | Google Trends API | B | 2026-09-05 |
| `eczema trigger tracker` | **0** | 0 (max 6) | n/a | Google Trends API | B | 2026-09-05 |
| `eczema triggers` | 1.9 | 0.6 | n/a | Google Trends API | C | 2026-09-05 |
| `dairy free breastfeeding` | 0.9 | 0.2 | n/a | Google Trends API | C | 2026-09-05 |
| `elimination diet breastfeeding` | 0.1 | 0.04 | n/a | Google Trends API | C | 2026-09-05 |
| `baby eczema dairy` | 0 (max 1) | **0** | n/a | Google Trends API | C | 2026-09-05 |
| `baby eczema cream` | **17.9** | **42.0** | n/a | Google Trends API | D | 2026-09-05 |
| `baby eczema foods to avoid` | 0.04 | 0.3 | n/a | Google Trends API | D | 2026-09-05 |
| `eczema food triggers` | 0.1 | 0.2 | n/a | Google Trends API | D | 2026-09-05 |
| `baby eczema diet` | 0.04 | 0.2 | n/a | Google Trends API | D | 2026-09-05 |
| `eczema food diary app` | **0** | **0** | n/a | Google Trends API | D | 2026-09-05 |
| `baby tracker app` | 15.2 | 3.1 | n/a | Google Trends API | E | 2026-09-05 |
| `eczema app` | 11.1 | 5.6 | n/a | Google Trends API | E | 2026-09-05 |
| `food diary app` | 6.8 | 4.4 | n/a | Google Trends API | E | 2026-09-05 |
| `eczema tracker app` | 0.02 (max 7) | **0** | n/a | Google Trends API | E | 2026-09-05 |
| `eczema diary` | 0.02 (max 7) | 0.2 (max 50) | n/a | Google Trends API | E | 2026-09-05 |

Batches: **A** core, **B** the ticket's exact phrases, **C** dairy/elimination, **D** intent mix (cream vs food), **E** app/tracker category. **X** is the mixed-geo request that puts US and GB series on one scale.

The three readings that matter in that table:

1. **Every phrase describing the product** (`eczema food diary`, `eczema trigger tracker`, `eczema food diary app`, `breastfeeding diet eczema`) is flat zero over five years in both countries. Not low — below the Trends reporting floor.
2. **Treatment beats causation by ~400x in the US.** Batch D: `baby eczema cream` 17.9 vs `baby eczema foods to avoid` 0.04. In the UK the ratio is ~140x (42.0 vs 0.3) — food is a slightly larger share of UK attention, but only slightly.
3. **The related-query evidence agrees.** Trends `RELATED_QUERIES` for `baby eczema` returns, US: `eczema on baby`, `baby eczema cream`, `eczema cream`, `aveeno baby eczema`, `aveeno eczema`, `eczema in baby`, `aveeno baby`, `baby face eczema`. UK: `eczema on baby`, `eczema cream`, `eczema in baby`, `cream for baby eczema`, `eczema rash baby`, `baby rash`, `eczema rash`, `baby with eczema`. **No food, diet, dairy, trigger, diary or tracking query appears in either top-8.** Parents in this niche search for a cream.

## Long tail (Google Suggest, 2026-09-05, US IP)

The phrases *do* exist as queries even where Trends cannot measure them — autocomplete is evidence of existence, never of volume.

- `baby eczema food` → `baby eczema food allergy`, `baby eczema foods to avoid`, `baby eczema food triggers`, `baby eczema food allergy breastfeeding`, `baby eczema food intolerance`, `baby eczema food allergy reddit`, `child eczema foods to avoid`, `baby eczema diet`
- `eczema food diary` → `eczema food diary app`, `eczema food plan`, `eczema food journal`, `eczema food log`, then it drifts to `does dairy affect eczema`, `can dairy cause eczema`, `is dairy bad for eczema`, `can food cause eczema`
- `eczema food trigger` → `...adults`, `...baby`, `...in toddlers`, `...reddit`, `...list`, `...test`, `common eczema food triggers`
- `breastfeeding diet eczema` → `breastfeeding diet eczema baby`, `elimination diet breastfeeding eczema`, `foods to avoid while breastfeeding baby with eczema`, `can a breastfeeding moms diet affect her baby's eczema`
- `baby eczema dairy` → `...dairy allergy`, `...dairy intolerance`, `...dairy reddit`, `baby eczema milk allergy`, `baby eczema milk protein allergy`
- `elimination diet breastfeeding` → `...gas`, `...reflux`, `...meal plan`, `...eczema`, `...reddit`, `...baby eczema`, `...colic`
- `eczema tracker` → `eczema tracker app`, `my eczema tracker`, `eczema symptom tracker`, `eczema food tracker`, `eczema flare tracker`, `best eczema tracker app`
- `eczema diary` → `eczema diary app`, `eczema food diary`, `eczema food diary app`, `eczema symptom diary`, `eczema trigger diary`, `eczema flare up diary`
- `food diary app eczema` → `food diary app for eczema`, `food diary app for allergies`, `food diary app for elimination diet`, `food diary app for intolerance`
- `eczema trigger tracker app` → **no suggestions returned at all.** Do not use that phrasing anywhere in the landing page or ASO copy; it is not language anyone types.

Two patterns worth carrying into #8 (ICP / promise) and #10 (copy):

- **The searched form is a question, not a tool.** `can dairy cause eczema`, `does dairy affect eczema`, `can a breastfeeding moms diet affect her baby's eczema`, `baby eczema caused by dairy`. Parents search for an *answer*, not for a *tracker*.
- **`reddit` is a completion on almost every stem** (`baby eczema food allergy reddit`, `eczema food triggers reddit`, `baby eczema dairy reddit`, `elimination diet breastfeeding reddit`, `baby eczema causes reddit`, `breastfeeding eczema reddit`). Corroborates #2's premise that the discussion lives in forums, and points at Reddit as the channel to weigh in #6.

## Seasonality — real, and it is a *summer trough*

Google Trends 5-year weekly series, averaged by calendar month, `baby eczema` (index):

| | Jan | Feb | Mar | Apr | May | Jun | Jul | Aug | Sep | Oct | Nov | Dec |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| US | 47.9 | 43.1 | 46.0 | **50.1** | 45.8 | 41.6 | 35.5 | 32.5 | **32.1** | 33.3 | 37.6 | 39.4 |
| GB | 68.2 | 71.2 | **77.6** | 76.1 | 66.3 | 56.0 | 45.5 | 42.5 | **39.3** | 44.8 | 54.1 | 56.0 |

Peak-to-trough: **1.56x** US (Apr vs Sep), **1.97x** UK (Mar vs Sep). `baby eczema cream` follows the same shape (US 27.8 Apr → 11.5 Sep, **2.4x**; GB 58.7 Mar → 27.3 Jul/Sep, **2.2x**).

**A traffic test run now (early September) lands in the annual floor** — the worst four weeks of the year in both countries, and roughly half of March/April interest in the UK. That is a direct input to #7's pass/fail bar: either run the test in Feb–Apr, or set the bar knowing the sample is drawn from the trough. Do not compare a September result against a bar calibrated on a spring number.

Independent corroboration of a seasonal shape (different metric, global not per-country, so magnitude is not comparable): Wikimedia Pageviews REST API for `en.wikipedia/Atopic_dermatitis`, user traffic, monthly Aug 2025–Aug 2026 — 657,206 views over 13 months, mean 50,554/month, ranging 78,827 (Oct 2025) down to 23,884 (Aug 2026).

## Traffic cost

No per-keyword CPC was obtainable free (see method). Industry benchmarks, each from the primary publisher:

| Figure | Value | Source | Sample |
|---|---|---|---|
| Google Ads avg CPC, all industries | **$5.42** | WordStream, *Google Ads Benchmarks 2026*, pub. 2026-05-19 | 13,474 US search campaigns, 2025-04-01 → 2026-03-31 |
| Google Ads avg CPC, Physicians & Surgeons | $4.76 (CTR 6.61%, CVR 12.43%, CPL $40.04) | same | same |
| Google Ads avg CPC, Dentists & Dental | $8.00 | same | same |
| Google Ads avg CPC, all-industry CPL | $66.69 (CTR 6.64%, CVR 8.18%) | same | same |
| Healthcare search avg CPC, overall | $5.64 (+6% YoY) | LocaliQ, *Healthcare Search Ads Benchmarks for 16 Specialties*, pub. 2026-01-13 | 3,542 US campaigns, 2024-10-01 → 2025-09-30 |
| Healthcare search, **Dermatology** | CPC **$4.90**, CPL $18.54, CVR 25.33% | same | same (min 43 campaigns/subcategory; medians) |
| Facebook Ads, traffic objective, all industries | CPC **$0.70** (CTR 1.71%) | WordStream, *Facebook Ads Benchmarks 2025*, pub. 2025-09-15 | 554 US traffic campaigns, 2024-04-01 → 2025-06-30 |
| Facebook Ads, traffic, Health & Fitness | CPC **$0.80** (CTR 1.63%) | same | same |
| Facebook Ads, traffic, Physicians & Surgeons | CPC $0.82 (CTR 0.83%) | same | same |
| Facebook Ads, leads objective, all industries | CPC $1.92, CPL $27.66, CVR 7.72% | same | 726 US leads campaigns, same window |
| Facebook Ads, leads, Health & Fitness | CPC $2.64, CPL $52.98 | same | same |

WordStream's latest Facebook report is the 2025 edition; `wordstream.com/blog/facebook-ads-benchmarks` 301-redirects to the 2024 post and no 2026 Facebook URL exists (checked 2026-09-05), so the 2025 figures are current as published. WordStream and LocaliQ are the same data operation, which is why their healthcare numbers are consistent rather than independent — treat them as **one** source, not two agreeing ones. Both are **US** samples; no free UK CPC benchmark of comparable provenance was found, and UK CPCs should not be assumed equal to US.

**What $150 buys**

| Channel | CPC used | Clicks for $150 |
|---|---|---|
| Google Search, all-industry | $5.42 | **~27** |
| Google Search, healthcare overall | $5.64 | ~26 |
| Google Search, dermatology | $4.90 | ~30 |
| Meta traffic, all-industry | $0.70 | **~214** |
| Meta traffic, Health & Fitness | $0.80 | ~187 |

Also measured, and it cuts both ways: **Bing served zero ad slots** on `eczema food diary`, `baby eczema food triggers` and `eczema tracker app` (`cc=US`, 2026-09-05 — HTML fetched and ad markers counted, 0 of 3). Nobody is bidding on these terms. Cheap clicks, yes — but the reason they are cheap is that there is nothing there to buy.

## The read: is the intent real, or is the problem felt but not searched?

**Felt, but not searched — and the distinction is unusually clean here.** The condition generates large, seasonal, five-year-stable demand in both countries, and the food-causation question is genuinely live in parents' heads: Google Suggest completes `can dairy cause eczema`, `does dairy affect eczema`, `baby eczema caused by dairy` and `can a breastfeeding moms diet affect her baby's eczema` without prompting, and `elimination diet breastfeeding eczema` is a real completion. But the *tracking* framing has no search footprint whatsoever — `eczema food diary`, `eczema trigger tracker`, `eczema food diary app` and `breastfeeding diet eczema` are flat zero on Trends across five years in both US and GB, `eczema trigger tracker app` produces no autocomplete at all, and the top-8 related queries for `baby eczema` in both countries are entirely cream and product queries with not one food, diet or tracking term among them. Parents search for a *cause* and for a *cream*; they do not search for a *diary*. That means the demand exists but is not addressable by keyword-intent capture, which is exactly the shape of niche where a search-ads test measures nothing: at $4.90–$5.64 healthcare CPC, $150 is ~26–30 clicks, and it would have to be spent on head terms like `baby eczema` whose searchers want a treatment, not a logging app — so a low conversion rate would tell you about mismatched intent rather than about the product. If a paid test runs at all it should run on **Meta interest targeting** (~$0.70–$0.80/click → ~190–215 clicks for $150, WordStream 2025), where the pitch can be made to a *demographic* rather than answered to a *query* — and #6's channel decision should weigh Reddit seriously, given how consistently `reddit` appears in the autocomplete tail. Two hard consequences for the rest of the map: **SEO/ASO cannot be the acquisition story** for a product named as a tracker, and **a September test sits in the annual trough** (US 1.56x, UK 1.97x peak-to-trough), so #7's bar must either be set for trough conditions or the test moved to Feb–Apr.

## Open, and cheap to close

- **Absolute monthly volumes and per-keyword CPCs are missing.** One human with a Google Ads account can paste the keyword list above into Keyword Planner and fill both columns in ~5 minutes, no spend required. Until then no monthly-search figure should appear anywhere downstream of this file.
- **UK Suggest data is not actually UK data** (`gl=uk` ignored). If the UK long tail matters to #10's copy, it needs a UK-IP run or Keyword Planner with UK geo.
- **No independent second source for CPC.** WordStream and LocaliQ are one operation. A UK-specific CPC benchmark from an unrelated publisher would be worth having before #12 commits the money.
