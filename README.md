# cheapest proxies: how to compare per-IP vs per-GB pricing and pick a residential plan that fits your real volume

Anyone searching for the cheapest proxies is usually running into the same wall about ten minutes in. Every provider's homepage quotes a rate, and that rate belongs to a tier almost nobody buys. You want 5 GB this month, and the number that sold you on the site is the one that requires 5,000 GB to unlock.

So the honest starting point is this: there is no cheapest residential proxy provider. There's a cheapest provider *at your volume*, and the answer moves a lot depending on whether you're pushing 5 GB, 100 GB, or half a million IPs. The useful skill isn't finding a low number. It's matching the billing unit to how your workload actually consumes.

Below is how the pricing math works, a full current price sheet from one provider worth using as a worked example — 9Proxy — and the fine print that decides whether the cheap option stays cheap once you're using it.

## The headline rate is almost never your rate

Pull a few published entry rates and the pattern is hard to miss. Oxylabs' smallest residential plan is $30/month for 5 GB, which works out to $6/GB. Bright Data lists $8/GB and discounts to $4/GB pay-as-you-go. IPRoyal's navigation advertises "from $1.75/GB" while its cheapest publicly listed tier is $4.90/GB at 50 GB. Rayobyte's $0.50/GB requires a 5,000 GB commitment.

None of those numbers are lies. They're just answered at a volume you may never reach.

The flip side matters just as much. A flat-rate provider like DataImpulse sells at $1/GB with a $5 minimum — which beats nearly every subscription at small volume, and gets beaten badly by volume tiers above roughly 200 GB. Evomi's entry plan is 100 GB, so at 5 GB/month you're paying for 95 GB you'll never touch. SOAX doesn't sell plain gigabytes at all; the same gigabyte burns different credit amounts depending on the country tier of the IP.

Two rules fall out of that:

- **Under ~50 GB/month, plan granularity beats unit price.** If the smallest plan is 100 GB, your real rate is whatever you paid divided by what you used.
- **Above ~200 GB/month, unit price takes over again**, and the floor moves to whoever gives the deepest volume discount.

Per-IP providers sit sideways to all of this, which is where things get interesting.

## Two billing models that don't convert into each other

Residential proxies get sold two ways, and comparing them by "price" alone is a category error.

**Per-gigabyte, rotating IPs.** You buy traffic. Every request or session can come out of a different IP in the pool. Great for wide geo coverage, distributed requests, keyword and SERP checks, ad verification, lightweight scraping where each page is small. Your cost scales with bytes, which is fine until pages get heavy — a JavaScript-rendered page at 2–5 MB each turns a 100,000-page job into real money.

**Per-IP with unlimited bandwidth.** You buy addresses, not traffic. A fixed price per IP, and you can push as much data through it as you want while it's alive. This is the model that wins when bandwidth is unpredictable or heavy: media-adjacent scraping, long sessions that need to hold one identity, bulk transfers through few exits. The catch is that residential IPs don't live forever — hours, sometimes most of a day — so the "unlimited" clock is running while it's up.

Buying IPs when you need bandwidth wastes money. Buying bandwidth when you need 800 stable sessions wastes more, because you end up reconciling sessions by hand against a traffic meter.

## What the cheapest end of the market actually looks like today

9Proxy is a reasonable example to price out because it sells both models side by side, so you can see the units next to each other. It's a residential proxy network advertising 20M+ IPs across 90+ countries, HTTP/HTTPS and SOCKS5 support, IPv4 only, and targeting down to country, city, ZIP code and ISP level. It's pay-as-you-go — no monthly subscription you have to remember to cancel.

One thing worth knowing before you look at prices: 9Proxy raised them. On 18 May 2026 the company announced the first pricing adjustment in its three-year history, effective 1 June 2026, covering **IP-based packages and bundle packages**. GB-based packages were left alone. Because unused IPs don't expire on that platform, anything bought before the change stayed at the old, lower rate.

The current floors are **$0.018 per IP** at the 500,000-IP tier, and **$0.68 per GB** at the 10,000 GB tier. Per-unit figures on the price sheet are rounded, so a couple of totals don't divide out exactly.

### IP-based residential packages (unlimited bandwidth per IP)

| Package | Price per IP | Total | Notes |
| --- | --- | --- | --- |
| 100 IPs | $0.24 | $24 | Smallest entry point |
| 500 IPs | $0.144 | $72 |  |
| 1,000 + 500 bonus IPs | $0.084 | $126 | 1,500 IPs total; flagged as the popular tier |
| 2,500 IPs | $0.084 | $210 |  |
| 5,000 IPs | $0.072 | $360 |  |
| 15,000 IPs | $0.048 | $720 |  |
| 25,000 IPs | $0.035 | $863 |  |
| 50,000 IPs | $0.029 | $1,438 |  |
| 100,000 IPs | $0.023 | $2,300 | Business tier |
| 200,000 IPs | $0.021 | $4,140 | Business tier |
| 500,000 IPs | $0.018 | $8,625 | Business tier |

👉 [See the current per-IP package pricing](https://bit.ly/9-Proxy)

Bandwidth is unmetered on every row. Unused IPs don't expire.

### GB-based residential packages (rotating IPs)

| Package | Price per GB | Total | Validity |
| --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | 180 days |
| 50 + 5 bonus GB | $2.10 | $105 | 180 days |
| 100 GB | $1.50 | $150 | 180 days |
| 200 GB | $1.00 | $200 | 180 days |
| 1,000 GB | $0.80 | $800 | 180 days |
| 2,000 GB | $0.75 | $1,500 | 180 days |
| 3,000 GB | $0.72 | $2,160 | No expiry |
| 6,000 GB | $0.70 | $4,200 | No expiry |
| 10,000 GB | $0.68 | $6,800 | No expiry |

👉 [Compare the GB-based tiers side by side](https://bit.ly/9-Proxy)

The 180-day window matters more than it looks. Most traffic-based providers force unused gigabytes into a 30-day box, which is a quiet tax on anyone whose workload is lumpy — a big scraping sprint, then two quiet weeks. The three enterprise tiers remove the deadline entirely.

### Bundle packages (IPs plus bandwidth)

| Bundle | Price | What it covers |
| --- | --- | --- |
| 100 IPs + 5 GB | $30 | Entry bundle |
| 1,500 IPs + 50 GB | $180 | Mixed workloads |
| 5,000 IPs + 500 GB | $720 | Heavier mixed workloads |

👉 [Check the bundle options](https://bit.ly/9-Proxy)

Do the arithmetic and the bundle logic is visible. 100 IPs alone costs $24; the $30 bundle throws in 5 GB of rotating traffic for $6 more. On the top end, 5,000 IPs alone is $360, and $720 buys the same address pool plus 500 GB.

## How to decide, in plain terms

**If your monthly volume is genuinely small — a few gigabytes — buy flat-rate gigabytes elsewhere.** 9Proxy's 5 GB tier is $15, or $3/GB. A flat $1/GB provider sells 5 GB for $5. There's no spin that makes $15 cheaper than $5. Volume-discount curves are designed for growth; at tiny volumes they're just a ceiling you haven't reached yet.

**If you're landing somewhere around 100–200 GB, the tiers start to matter.** At 200 GB you're at $1/GB, at 2,000 GB you're at $0.75, and past that it's grinding down toward $0.68. Below 50 GB, a flat-rate vendor usually still wins.

**If bandwidth is heavy or unpredictable, stop shopping by the gigabyte and buy IPs.** A per-IP plan with unlimited traffic means a 4 MB page and a 40 KB page cost the same. That single change removes the cost volatility that makes scraping budgets impossible to forecast. It's the strongest argument for the per-IP side of this market, and it's why the 1,000 + 500 tier gets the "popular" label — 1,500 IPs at $0.084 each is where the per-unit cost drops hard without a five-figure commitment.

**If you need both — stable sessions for some tasks, wide rotation for others — the bundle rows exist precisely for that.**

The one decision that overrides all the pricing: measure success rate on your own targets before you scale. A pool that costs 20% less and fails 15% more often is not cheaper. Every published per-unit rate in this market, including the ones above, is an advertised rate rather than a measured outcome.

## What you're setting up, and what it needs

Access method differs by model, and it affects whether the cheap plan is convenient or annoying.

**IP-based plans require the desktop app** (Windows), which routes traffic at the OS layer through local port forwarding. It works with software that has no native proxy settings, and there's an auto-rotation proxy option that switches IPs at intervals you define on selected ports. Each IP runs for a few hours, occasionally up to around 24 hours. Unused IPs sit in your balance indefinitely.

**GB-based plans don't need the app.** You authenticate with username and password or an IP whitelist and pull straight from the dashboard, in rotating mode (new IP per request or session) or sticky mode (one IP held for a configured session length). That's the friendlier path if you just want to drop a proxy string into a script or a browser.

There's also Proxy2Web for zero-install browser work, ProxyHub for mobile device management, and a public API for session control and usage stats from code. Third-party integrations are standard SOCKS5, so anti-detect browsers, proxychains and Python scripts work without protocol gymnastics.

## The fine print that changes the math

Four things decide whether a cheap plan stays cheap. All of them live in the terms, not the price table.

**No refunds, and wallet funds don't come back out.** 9Proxy's refund policy, last updated June 2025, is explicit: services are intangible and all purchases and deposits are final, including 9Proxy Wallet deposits. Once credentials are issued, nothing gets reversed. Wallet balances don't expire while your account is in good standing.

**Failed proxies get replaced, not refunded.** If a proxy dies within the first 60 seconds of use, it's automatically replaced after you check its status in the app's "Today List." That's a better deal than most providers offer — a dead connection is normally just a consumed resource — but it's a credit mechanic, not a money-back guarantee.

**The Today List saves real money.** Proxies you've already accessed in the last 24 hours can be reused at no extra charge, which is worth roughly 20–30% off effective spend on workloads that revisit the same territories. It's a bigger discount than a lot of coupon codes floating around.

**Trials are limited and conditional.** 9Proxy offers new users a limited trial depending on availability, requested through support, so you need to ask rather than click a "free trial" button. There's no permanently available free tier. Anyone wanting a true zero-spend evaluation period will find this a gap — competitors like Webshare do offer a free 10-IP plan, and Bright Data and Oxylabs run free trials for registered businesses.

One more caveat worth flagging: third-party review coverage reports that 9Proxy has signaled a policy shift away from media streaming on IP-based plans under an updated acceptable use policy. If streaming is your use case, confirm the current terms with support before paying.

Payments accepted include credit cards, crypto (USDT, BTC, ETH, LTC, DOGE and others), bank cards, Alipay, Apple Pay and Google Pay — relevant if you're buying from a region where card acceptance is a hassle.

## What third-party sources say

The vendor publishes a 99.95% uptime figure and a 4.6/5 "Excellent" rating on Trustpilot. Treat the uptime number as marketing until you've tested it against your own targets.

Independent comparison coverage is more mixed, and more useful. ProxyLook rates 9Proxy 3.9/5 with a trust score of 7.8/10, reports a 97% capture success rate and average response time of about 1,300 ms, and notes the two recurring complaints: the narrow credit-refund terms and the absence of a clearly advertised free trial. Trustpilot reviews echo that — the positive ones cluster around the replacement policy and pricing, the negative ones around buyers who picked the wrong model (usually someone expecting rotating datacenter-style proxies who landed on residential-only) and then couldn't recover their spend. Geekflare's review documents the June 2026 price adjustment alongside the plan breakdown.

That's a fair summary of a budget provider: the mechanics are genuinely better than average, and the risk is concentrated in the buying decision rather than in the service. Which is why the refund policy is worth reading before you click, not after.

## The traps that make "cheap" expensive

**Free proxy lists.** Shared datacenter IPs, publicly scraped, already blacklisted. Your time is not that cheap.

**Datacenter proxies for residential-guarded targets.** Half the price, and blocked before your request reaches the application layer. Wrong tool, not a cheaper version of the right tool.

**Buying the biggest tier to get the best rate.** The floor price always requires the largest commitment. Buy the smallest package that covers a real workload, measure success rate on your actual targets, then scale. Every provider's own guidance says this, and it's the one piece of advice in this market that's both free and correct.

**Ignoring expiry.** A cheap per-GB rate with a 30-day window can cost more in practice than a slightly higher rate with 180-day validity. Compare what you'll actually consume, not what you bought.

## Quick answers

**What's the cheapest way to buy residential proxies?** Per-gigabyte pricing with a flat rate and no minimum, if you stay under ~50 GB/month. Per-IP with unlimited bandwidth once traffic gets heavy or unpredictable — that's where the per-unit cost stops mattering.

**Is 9Proxy actually cheap?** Its entry tiers aren't the market floor — the 5 GB tier at $3/GB is beaten by flat-rate vendors. Its floor of $0.018/IP and $0.68/GB is competitive at the top end, and unlimited bandwidth per IP is where the value sits for bandwidth-heavy work.

**Does it have a free trial?** Limited and availability-based, requested through support. No always-on free tier.

**Can I get a refund if it doesn't work out?** No. Replacements and credits for dead IPs within 60 seconds, but all purchases and wallet deposits are final.

## The bottom line

Cheapest proxies isn't a provider, it's a filter you apply to your own numbers. Work out your monthly gigabyte volume, decide whether you're buying addresses or traffic, then compare only the tiers that actually cover that volume — and check the refund and expiry terms before the price, because those two clauses decide what the sticker price is worth.

If your workload is bandwidth-heavy, unpredictable, or needs a lot of stable sessions at a low per-unit cost, 👉 [the per-IP packages currently start at $24 for 100 IPs with unlimited traffic](https://bit.ly/9-Proxy). If you're scraping a few gigabytes a month, do the flat-rate comparison first — it'll probably win, and knowing that is worth more than a coupon.

9Proxy's affiliate materials advertise a 5% discount for referred users, and the invite-code sign-up flow is how that gets attached to the account. Either way, buy the smallest tier that tests your real targets. It's the cheapest thing you'll do all quarter.
