# Bright Data Pricing: What Each Proxy Type Really Costs, Where the $8/GB Goes, and How to Cut the Bill

Search "bright data pricing" and you get three different numbers before you finish your coffee. The pricing index says residential starts at $2.50/GB. The residential page itself shows $8/GB on the pay-as-you-go card. Somewhere on a banner there's a coupon that halves it for a quarter. All three are technically true and none of them is what most people end up paying.

So here's the version with the meters spelled out: what each proxy type costs, why the headline rate is misleading, which costs never make it onto the pricing cards, and where the money is better spent if you're not running an enterprise data operation.

Prices below reflect Bright Data's published rates as reported through late September 2026, plus what third-party breakdowns found when they read the same pages. Where sources disagree, I say so rather than picking the flattering number.

## The 30-second version: what Bright Data charges

| Product | How you're billed | Entry rate |
| --- | --- | --- |
| Residential rotating | per GB | $8/GB pay-as-you-go (list), down to $5/GB on the $1,999/month tier |
| Datacenter, shared | per IP | $1.40/IP at 10 IPs → $0.90/IP at 1,000 IPs |
| Datacenter, dedicated | per IP | $2.20/IP at 10 IPs → $1.30/IP at 1,000 IPs |
| Datacenter, shared | per GB | $0.60/GB pay-as-you-go → $0.42/GB on the 5 TB tier |
| ISP (static residential) | per IP | from $18/month for 10 shared IPs; ~$1.45/IP at 100 IPs |
| Mobile (4G/5G) | per GB | around $8.40/GB per PCMag's comparison; other breakdowns put pay-as-you-go nearer $20/GB |
| Web Unlocker | per request | about $1.50 per 1,000 requests on pay-as-you-go |
| Free resources | — | trial credits on signup plus 5,000 recurring monthly credits for the API products |

Two structural facts matter more than any single rate. Bright Data has no free plan — you get trial credits and then you pay. And the policy applies to datacenter, ISP, residential and mobile networks alike, so you can run anything on pay-as-you-go without a monthly commitment if you'd rather keep the flexibility.

## Why "starting from $2.50/GB" isn't the price you'll pay

Bright Data publishes one pricing index and a separate pricing page per product, and the index quotes a starting price that often doesn't exist on the page it links to. One write-up that read every pricing page on the site in September 2026 found three products where the menu number and the card number diverge.

Residential is the clearest case:

- The index says 50% off, from $2.50/GB.
- The residential page's own meta description says "starting from $5.88/GB".
- The plan cards say $8/GB pay-as-you-go, or $4/GB with the RESIGB50 coupon.
- The $2.50 figure is the $1,999/month, 798 GB tier **with the coupon applied** — which works out to $2.51/GB.

Nobody buying 10 GB is offered $2.50/GB. That number belongs to a customer committing roughly $24,000 a year. It's not deception so much as a pricing page built to lead with the best case, and it's worth internalising before you build a budget around a headline rate.

## Residential proxies: the four plans people actually compare

| Plan | Monthly cost | Bandwidth included | List rate | Rate with RESIGB50 |
| --- | --- | --- | --- | --- |
| Pay as you go | $0 | none included | $8/GB | $4/GB for 3 months |
| Entry commitment | $499 | 141 GB | ~$7/GB | ~$3.54/GB |
| Mid tier | $999 | 332 GB | ~$6/GB | ~$3.01/GB |
| Top tier | $1,999 | 798 GB | ~$5/GB | ~$2.51/GB |

The coupon halves residential rates for three months. In month four, a $499 plan reverts to roughly $7/GB unless you renegotiate — that's the part the promotional banner doesn't say out loud.

Three other things belong in the same paragraph. Monthly commitments don't roll over, so unused gigabytes are gone at the end of the cycle. Bandwidth is billed by the megabyte including request and response headers, not just page content, with no rounding up. And residential plus mobile networks require KYC: Bright Data's own FAQ says a representative may ask for a short video call and company or personal verification before you can use them.

## Datacenter and ISP: the cheap end of the meter

If your targets aren't hardened, this is where Bright Data gets genuinely cheap, and the layout of the datacenter page tells you why. The same 1.3-million-IP pool is sold three ways.

**Shared, per IP:** 10 IPs at $1.40 each ($14/month), 100 at $1.00 ($100), 500 at $0.95 ($475), 1,000 at $0.90 ($900).

**Dedicated, per IP:** 10 at $2.20 ($22), 100 at $1.70 ($170), 500 at $1.50 ($750), 1,000 at $1.30 ($1,300).

**Shared, per GB:** $0.60 pay-as-you-go, then $0.51 (1 TB for $499), $0.45 (2 TB for $999) and $0.42 (5 TB for $1,999).

The per-IP plans are labelled unlimited, and the FAQ defines that word: each IP carries a 100 GB monthly fair-use allowance, pooled across the zone. Overflow it and you're back on per-GB pricing. That's roughly a 13x difference against residential for anyone whose targets don't need household IPs.

ISP proxies sit in between — static IPs leased from consumer ISPs, billed per IP rather than per GB. Shared ISP starts at $18/month for 10 IPs and drops to about $1.45/IP at the 100-IP tier, with dedicated ISP at $35/month for 10. Costbench lists ISP entry at $1.30/IP, which lines up with the volume end of that ladder.

## Mobile and managed APIs: the expensive corner

Mobile 4G/5G is the priciest proxy type on the market and Bright Data prices it accordingly. PCMag's comparison lists mobile at $8.40/GB; a separate pricing guide puts pay-as-you-go nearer $20/GB with committed rates from about $7/GB. Treat anything in that band as a number to confirm with sales rather than a rate you can plan against, because mobile is reserved for targets that block everything else.

Then there's the done-for-you layer: Web Unlocker at roughly $1.50 per 1,000 requests on pay-as-you-go, with overage on the $499 Scale plan at $1.30 per 1,000. SERP and Web Scraper APIs are billed per request or per record instead. If you'd rather not babysit rotation logic and CAPTCHA handling, this is the tradeoff — more per unit, less engineering.

One genuinely useful detail buried in the docs: every new account gets a recurring free tier of 5,000 credits a month across Web Unlocker, SERP API, Web Scraper API and Scraper Studio, and it renews monthly. That's not a trial that dies after seven days.

## Costs that never make it onto a pricing card

- **No rollover.** A $499 commitment bills flat whether you use 141 GB or 40. The tiers are flat-fee, not prepaid balance.
- **Targeting is contested.** Bright Data's residential cards list country, state, city and ZIP targeting as included at no extra charge. At least one independent breakdown reports city or ZIP targeting adding a 20–40% multiplier, and Vendr's procurement data also treats premium targeting as a cost driver. Those two accounts don't reconcile, and I'd ask before assuming either.
- **KYC.** Residential and mobile access can require identity verification. Budget a day, not an afternoon.
- **The enterprise wall.** Above roughly 1 TB a month, pricing goes to quote. Vendr data suggests overage runs 20–50% above your contracted rate, which is exactly why a 20–30% buffer on your first commitment is the standard advice.
- **Payment friction.** Credit cards (Visa, Mastercard, Amex), wire transfer, Alipay, Payoneer, Google Pay, Apple Pay and Amazon Marketplace are all supported. Cryptocurrency is not, which rules out anonymous purchasing.

## Pay as you go or commit? Do the arithmetic first

At list rates, the $499 tier makes sense once you'd otherwise be buying somewhere around 62 GB a month at $8/GB — that's where the two bills cross. Below that, pay-as-you-go wins.

Run a year of a 20 GB/month habit and the picture gets uncomfortable: three months at the promotional $4/GB costs $240, then nine months at $8/GB costs $1,440. That's $1,680 for 240 GB, an effective $7/GB for the year. Anyone buying that volume from a budget residential provider at roughly $1–3/GB pays a few hundred dollars for the same bandwidth. Bright Data's floor isn't the problem there; the entry tier is simply priced for a customer fifty times bigger.

Where the premium does earn itself back is on hardened targets. If your work involves aggressive bot management, pass rates matter more than per-GB rates, and a cheap proxy failing a third of requests is not cheap. That's the honest case for paying Bright Data money.

## Where a budget residential network fits

That leaves a large group in the middle: people who need residential IPs, don't need ISO-grade procurement paperwork, and wince at $8/GB. This is the slot 9Proxy is built for.

9Proxy runs a residential network of 20 million-plus IPs across 90-plus countries on 8,000-plus servers, with HTTP, HTTPS and SOCKS5 support and state, city and ISP-level targeting on its bandwidth plans. It's a smaller pool than Bright Data's 400 million, and it doesn't pretend otherwise — the pitch is cleaner, cheaper IPs rather than the biggest network. Two mechanics are worth knowing before you compare prices: if a proxy fails within 60 seconds of activation, it's replaced at no charge, and anything you used in the last 24 hours can be reused free through the Today List.

The billing comes in three shapes, which is where it diverges from Bright Data's ladder:

- **Per GB**, with rotating IPs, for rotation-heavy jobs that don't burn much data.
- **Per IP**, with unlimited bandwidth, for long sessions where traffic is unpredictable.
- **Bundles**, mixing IPs and gigabytes for teams doing both.

One timing note that matters if you're comparing against older reviews: 9Proxy raised prices on its IP-based and bundle packages on June 1, 2026, its first adjustment ever, and explicitly left GB-based pricing untouched. Reviews written before that date quote lower per-IP numbers than what's on the order page now.

### 9Proxy GB-based packages

| Package | Effective rate | Total | Validity |
| --- | --- | --- | --- |
| 5 GB | $3.00/GB | $15 | 180 days |
| 55 GB (50 + 5 bonus) | $2.10/GB | $105 | 180 days |
| 100 GB | $1.50/GB | $150 | 180 days |
| 200 GB | $1.00/GB | $200 | 180 days |
| 1,000 GB | $0.80/GB | $800 | 180 days |
| 2,000 GB | $0.75/GB | $1,500 | 180 days |
| 3,000 GB | $0.72/GB | $2,160 | no expiry |
| 6,000 GB | $0.70/GB | $4,200 | no expiry |
| 10,000 GB | $0.68/GB | $6,800 | no expiry |

👉 [Check current 9Proxy bandwidth pricing](https://bit.ly/9-Proxy)

The 180-day window is the practical difference from a monthly commitment: irregular workloads aren't racing a calendar, and the top three tiers drop the deadline entirely.

### 9Proxy IP-based packages

| Package | Effective rate | Total | Notes |
| --- | --- | --- | --- |
| 100 IPs | ~$0.24/IP | $24 | unlimited bandwidth per IP |
| 500 IPs | ~$0.14/IP | $72 | — |
| 1,000 IPs + 500 bonus | ~$0.08/IP | $126 | the popular tier |
| 100,000 IPs | ~$0.02/IP | $2,300 | volume tier |
| 500,000 IPs | ~$0.017/IP | $8,625 | volume tier |

👉 [See 9Proxy's per-IP plans](https://bit.ly/9-Proxy)

The per-IP model is the one that catches people out in a good way: bandwidth is unlimited, so a heavy session costs the same as a light one. If your traffic is hard to forecast, that's a structurally different risk profile from per-GB billing.

### 9Proxy bundle packages

| Bundle | Total | Best for |
| --- | --- | --- |
| 100 IPs + 5 GB | $30 | testing both models at once |
| 1,500 IPs + 50 GB | $180 | mixed workloads, session persistence plus throughput |
| 5,000 IPs + 500 GB | $720 | larger operations routing through both modes |

👉 [Compare 9Proxy bundle options](https://bit.ly/9-Proxy)

Package prices are the ones published in mid-2026 third-party reviews and the company's own June 2026 pricing notice. Rates on proxy networks move, so confirm the figure on the order page before you commit — that advice applies to Bright Data's cards too.

## 9Proxy vs Bright Data, on the numbers that decide it

|  | Bright Data | 9Proxy |
| --- | --- | --- |
| Residential entry | $8/GB list ($4/GB on the 3-month coupon) | $3.00/GB at 5 GB |
| Cheapest residential rate | $5/GB list on the $1,999/month tier | $0.68/GB at 10,000 GB |
| Billing models | per GB, per IP, monthly commitments | per GB, per IP, bundles, no subscription required |
| Residential pool | 400M+ IPs | 20M+ IPs, 90+ countries |
| Targeting | country, state, city, ZIP (see the caveat above) | state, city, ISP on GB plans |
| Bandwidth expiry | monthly commitments don't roll over | 180 days, or no expiry on enterprise GB tiers |
| Free access | trial credits plus 5,000 recurring monthly API credits | no self-serve free trial, per Geekflare's 2026 review |
| Extra tooling | Web Unlocker, SERP API, Scraper Studio, datasets | proxy management app with auto-refresh, rotation, share codes |

Read down that table and the split is fairly clean. Bright Data is the right buy when you need the largest pool, managed unblocking for hostile targets, an account manager, and paperwork that survives procurement. It is a bad buy at 20 GB a month on easy targets, where the effective rate sits near $7/GB across a year and no tooling compensates for it.

9Proxy is the opposite profile: smaller network, no enterprise layer, and residential bandwidth at a fifth of the price or less. Some reviewers flag the smaller pool and the absence of a self-serve trial as real limitations, and both are fair — 20 million IPs is plenty for most scraping and multi-account work, but it isn't 400 million.

## Questions people ask before they buy either one

**Does Bright Data have a free trial?** Yes — every new signup gets trial credits usable across all products, and every account gets a recurring 5,000 monthly credits for the API products. There's no permanent free plan. 9Proxy has no self-serve trial; testing happens through community channels and its replacement policy.

**Does geographic targeting change the price?** Bright Data's documentation states that all countries are charged the same rate per GB. City and ZIP targeting is where sources disagree, as noted above.

**Is ISP traffic billed per GB?** No. ISP proxies bill per IP, and the unlimited label comes with a 100 GB per IP monthly fair-use allowance.

**Can I cap spending?** Yes — you can set a daily limit per zone by bandwidth or by dollars, and the zone suspends itself when it hits the cap. Allow 15 minutes of lag.

**What actually moves the bill?** Volume, product type and whether you commit. Datacenter bandwidth at $0.60/GB versus residential at $8/GB is the biggest single lever available, and it's the one most people ignore while shopping for a cheaper residential rate.

The short version: Bright Data's pricing is honest enterprise pricing with a confusing shop window. If you're near enterprise volume on hard targets, pay it. If you're not, the per-GB number you're comparing is doing most of the damage, and there's a whole tier of residential providers priced for the size you actually are.
