# united states proxy: how to get US residential IPs by state and city, verify them, and pick a plan that fits

Searching for a "united states proxy" usually means one of three things: you need a US IP to see what US users see, you need a lot of them to collect US data without getting blocked, or you need one that stays put long enough to keep an account alive. Those are different jobs, and they rarely get answered by the same product configuration.

Since geekflare-type reviews and provider comparison pages mostly rank vendors, they tend to skip the operational part: what targeting granularity you should actually request, how to check whether the IP you got is really residential, and what the session mode does to your success rate. That's the part that decides whether your US proxy works on Monday and dies by Wednesday.

9Proxy is a residential-only provider that's been mentioned a lot in 2025–2026 comparisons for one specific reason: you can buy by IP with unlimited bandwidth per IP, or by GB, and its targeting goes down to US state, city, ZIP, and ISP. Below is how its US targeting actually works, what the plans cost after the June 2026 price adjustment, and where a US residential proxy is the wrong tool.

## What a "United States proxy" can mean

Four product types get sold under the same phrase, and they behave differently:

- **Datacenter US proxy** — hosted in US data centers. Fast and cheap, but the ASN says "hosting provider," so anything with decent bot detection knows.
- **US residential proxy** — an IP assigned by a US consumer ISP to a real household connection. Passes IP reputation checks far more often. This is what 9Proxy sells.
- **US ISP / static residential** — a residential-registered IP running off hosted infrastructure. Stable for long sessions. 9Proxy does not offer this line.
- **US mobile proxy** — 4G/5G carrier IPs. Highest trust on social platforms, highest cost. Not part of 9Proxy's catalog either.

If you need a US mobile IP or a static ISP address, 9Proxy isn't the option. Its network is residential only, and that's the honest limit of the catalog.

## US targeting: country, state, city, ZIP, ISP

This is where most buying decisions get made badly. A US residential pool is not one bucket. 9Proxy's residential traffic is targeted through a structured username, so the location filter is something you type, not something you click:


subaccount-country-us-st-ohio-city-newyork-isp-as22773_Cox_Communications_Inc.-sst-15-ssid-ID1


Breaking that down: `country-us` routes through the United States, `st-ohio` narrows to a state, `city-newyork` narrows to a city (underscores replace spaces), `isp-as22773_Cox_Communications_Inc.` filters by ISP or ASN, `sst-15` sets a sticky session of 15 minutes, and `ssid-ID1` gives you a separate IP for parallel sessions under the same config.

The tradeoff is documented on 9Proxy's own side, and it's worth repeating because it's the single most common cause of "the US proxy I bought doesn't work": the more filters you stack, the thinner the pool gets. Country-only targeting is fastest and has the most IPs to draw from. Adding state, then city, then ISP each cuts the available set. Stacking state + city + ISP at once on a narrow metro is how people end up with repeated exits or timeouts and conclude the provider is bad.

Practical rule: pick the **least specific location that still satisfies your task**. If you're checking how a US page renders, country-level US is usually enough. If you're verifying local ad placements or store availability, you need city. ISP filtering matters when your target scores ISP reputation, not before.

## Is your US IP actually residential?

Check before you build a workflow on it. Connect through the proxy and load an IP intelligence page, then look at two things: whether the IP type reads as residential/ISP consumer rather than hosting, and what ASN is behind it. Cross-checking across two services is worth the 30 seconds.

On pool numbers, be skeptical of everything including the vendor. Third-party directories that have looked at this repeatedly point out that 9Proxy's promotional pages have claimed figures well above what independent reviews corroborate; the number that shows up consistently across 2025–2026 reviews is **20M+ residential IPs across 90+ countries**, reportedly grown from roughly 9 million after the BeeProxy merger. That's a workable pool, but it's smaller than the enterprise-tier providers, and IP density varies by country — the US is one of the stronger markets for this kind of network, but "stronger than average" is not "every ZIP code has depth."

Performance claims deserve the same treatment. 9Proxy publishes roughly 99.5% success rate, ~0.6s average response, and 99.95% uptime. Independent benchmark data puts the realistic range at about 97% success and ~1.3s P95 latency on rotating residential. Both numbers are plausible for the category; neither is an SLA.

## Matching the plan type to the job

Two billing models, and they map to two different kinds of work.

**IP-based (per IP, unlimited bandwidth).** You buy a count of residential IPs. Each one carries unlimited data for as long as it lives, which the provider describes as anywhere from a few hours up to about 24 hours. This is the model for session-stable work: keeping the same identity across hundreds of requests, long scraping runs where you can't predict traffic, account management, anything where you'd rather not watch a bandwidth gauge.

**GB-based (per gigabyte, unlimited endpoints).** You buy traffic and generate as many endpoints as you want while the balance lasts. IPs rotate without a fixed lifetime. This is the right shape for high-rotation work with light pages — SERP checks, price monitoring, API polling, lightweight scraping across many US locations. All GB plans carry 180-day validity, so unused balance doesn't evaporate at month end.

**Bundles** exist for teams that need both: a set of stable IPs plus a rotating traffic pool.

👉 [Compare 9Proxy's current packages before you pick a model](https://bit.ly/9-Proxy)

Third-party reviewers have noted 9Proxy does **not** ship a datacenter, ISP, or mobile line, and no managed unblocker/SERP API. If your targets are Amazon, Google at high frequency, or LinkedIn, a budget residential pool is not where those workloads go.

## All 9Proxy plans and current prices

On May 18, 2026, 9Proxy announced its first-ever price adjustment, effective June 1, 2026. It applies to IP-based packages and bundles; GB-based pricing was explicitly left unchanged.

### IP-based packages

| Package | Price per IP | Total |
| --- | --- | --- |
| 100 IPs | $0.24 | $24 |
| 500 IPs | $0.144 | $72 |
| 1,000 IPs (+500 bonus) | $0.084 | $126 |
| 2,500 IPs | $0.084 | $210 |
| 5,000 IPs | $0.072 | $360 |
| 15,000 IPs | $0.048 | $720 |
| 25,000 IPs | $0.035 | $863 |
| 50,000 IPs | $0.029 | $1,438 |
| 100,000 IPs (Business) | $0.023 | $2,300 |
| 200,000 IPs (Business) | $0.021 | $4,140 |
| 500,000 IPs (Business) | $0.018 | $8,625 |

Unused IPs in this model don't expire. The 1,000 + 500 bonus tier is the one the site itself flags as most popular, and the economics support that: it's the first tier where the effective per-IP rate drops hard without jumping into five-figure volumes.

### GB-based packages

| Package | Price per GB | Total | Validity |
| --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | 180 days |
| 50 GB (+5 bonus) | $2.10 | $105 | 180 days |
| 100 GB | $1.50 | $150 | 180 days |
| 200 GB | $1.00 | $200 | 180 days |
| 1,000 GB | $0.80 | $800 | 180 days |
| 2,000 GB | $0.75 | $1,500 | 180 days |

Volume pricing continues downward from there — the lowest published rate is $0.68/GB at the top 10,000 GB tier. Unlike IP-based purchases, GB balance does carry an expiry (180 days) unless you're on Enterprise.

### Bundle packages

| Bundle | Contents | Price |
| --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 |
| Popular | 1,500 IPs + 50 GB | $180 |
| Pro | 5,000 IPs + 500 GB | $720 |

### Enterprise

Custom pricing, with terms the standard tiers don't get: unlimited data validity, team mode for one owner plus up to five members, no-expiration bandwidth sharing inside the team, per-member traffic controls, activity logs, unlimited share codes, and a dedicated support channel. Enterprise GB packages are the only ones where bandwidth genuinely never expires.

👉 [See the full plan list and current pricing on 9Proxy](https://bit.ly/9-Proxy)

## Setting up a US proxy

Two authentication methods. **User-pass** is the flexible one: create sub-users, assign traffic to them, and generate credentials per sub-user — the usual setup for scripts, cloud jobs, and handing separate access to clients. **IP whitelisting** skips credentials entirely and instead lets a specific device IP connect straight through.

From there, the dashboard's Proxy Generator handles selection (country → state → city → ZIP → ISP), session mode, and export. You can pull endpoints as `.txt` or `.csv` or grab ready-made code samples. A minimal request through a US IP looks like this:

bash
curl -x yourproxyhost:yourport \
     -U "subuser-country-us-sst-15-ssid-bot01:yourpassword" \
     https://ipinfo.io


Client-side options, depending on what you're doing: a **desktop app** for Windows, macOS, and Linux that filters by country, state, city, ISP, or ZIP and can bind IPs to ports; **Proxy2Web**, a browser-based, zero-install route using standard user:pass credentials for quick manual checks; **ProxyHub** for mobile device management; and a **public API** for generating proxy lists, rotating IPs, checking wallet balance, and managing sub-users. HTTP/HTTPS and SOCKS5 are both supported, and SOCKS5 is what you want when you're wiring into anti-detect browsers or proxychains-style tooling.

Sticky sessions are set with `sst-<minutes>`. Each unique `ssid` gives you a different IP even when everything else in the string is identical — that's how you run parallel US sessions for, say, five accounts from one config without them sharing an exit node.

## Where a US residential proxy helps, and where it doesn't

**It helps for:**

- Collecting data from US sites where the region changes what's served — pricing, availability, search results, shipping options
- Ad verification — confirming your placements render for real US users in a specific state or metro
- Localized SEO and SERP checks, where a random global exit tells you nothing about the US market
- Managing multiple US-facing accounts where IP reputation at the ASN level matters
- Security testing, where you need clean residential IPs as a baseline rather than hosting ranges that get flagged at the IP layer before your payload is ever evaluated

**It doesn't help for:**

- **Streaming.** Major streaming platforms frequently block residential IPs regardless of provider quality, and 9Proxy has signaled under its Acceptable Use Policy that media streaming (YouTube and similar) is no longer supported on IP-based plans. If unblocking US Netflix is the actual goal, a residential proxy subscription is the wrong purchase, not just the wrong vendor.
- **Heavily protected targets at scale.** Budget residential pools land in the 70–85% success band on aggressive targets while enterprise providers advertise 98%+. Budget for retries or pick a different stack.
- **Mobile-specific platforms.** No mobile IPs in the catalog, so platforms that weight carrier ASNs heavily will be a harder fight.

## What to check before you buy

A few terms that matter more than the headline price:

**The 60-second replacement policy.** If an IP fails immediately, you check its status and get a replacement. That's the refund scope — it covers IPs that die almost instantly, not a change of mind about the service.

**Today List reuse.** IPs you've used in the last 24 hours can be reactivated at no extra IP cost if they come back online. For recurring daily jobs against the same sites, this quietly cuts your IP consumption.

**No clearly advertised free trial.** Trials have existed as promotions, but they aren't a standard feature, and the refund window is narrow. Treat your first purchase as the test: buy the smallest tier that covers your real workload and validate it against your actual US targets.

**Crypto payments carry a bonus.** Card, Apple Pay, Google Pay, Alipay, and regional rails are accepted; paying in crypto through CoinPayments adds a +5% IP bonus.

## FAQ

**Do I need GB-based or IP-based for US scraping?**
If pages are light and you want to rotate across many US locations, GB-based is usually cheaper. If each job needs the same IP across many requests, or bandwidth per request is heavy, IP-based with unlimited bandwidth per IP is the better fit.

**How many US locations can I target?**
Country, state, city, ZIP, and ISP-level filtering, expressed through the proxy username. ZIP and ISP filters are the narrowest and should be used only when your task specifically needs them.

**Can I use the same US IP for several accounts?**
You can hold an IP sticky with `sst-<minutes>`, and each distinct `ssid` yields a separate IP under the same configuration. Whether that's appropriate depends on the platform's rules, which are yours to check.

**Does 9Proxy offer US datacenter or mobile proxies?**
No. Residential only — country, state, city, ZIP, and ISP targeting within that.

👉 [Start with the smallest 9Proxy package and test it against your own US targets](https://bit.ly/9-Proxy)
