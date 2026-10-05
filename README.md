# Oxylabs pricing: what each plan actually costs per GB, where the bill climbs, and when a $1/GB pay-as-you-go plan makes more sense

If you're reading this, you probably already have a number in front of you. Maybe it says $4/GB. Maybe your checkout shows $6/GB. Maybe a colleague told you Oxylabs is the premium option and premium means "don't ask".

Oxylabs is genuinely one of the most capable proxy and scraping platforms on the market. It's also one of the harder ones to price, because it sells nine-ish different products, each with its own billing unit: per gigabyte, per IP, per successful result, per month. The per-GB rate on the residential product that everyone quotes is not the rate most buyers end up paying.

Here's the honest breakdown, plus the part most pricing pages on the internet skip: what you pay when your traffic volume doesn't fit neatly into a tier.

## The short version

> Oxylabs residential pricing is built around monthly commitment tiers. The cheapest per-GB rates sit behind the biggest commitments. If your usage is small or uneven, the effective rate you pay can be two to eight times the "from" price on the marketing page.

That's not a knock on the product. It's just how tiered pricing works, and it's worth understanding before you enter a card number.

## The residential ladder, tier by tier

Residential proxies are Oxylabs' flagship and the product almost everyone compares. The self-serve structure as it currently stands:

| Plan | Traffic per month | Monthly cost | Effective rate | Buy |
| --- | --- | --- | --- | --- |
| Pay as you go | from 1GB | usage-based | ~$8/GB standard, ~$4/GB on a capped promo | Not your link target here |
| Starter | 5GB | $30 | $6/GB | Not your link target here |
| Basic | 20GB | $100 | $5/GB | Not your link target here |
| Advanced | 125GB | $500 | $4/GB | Not your link target here |
| Corporate | 1TB | $2,500 | $2.50/GB | Not your link target here |
| Enterprise | above 1TB | custom quote | negotiated | Sales-led |

Two things stand out.

First, the pattern is predictable: commit more, pay less per GB. Going from the 5GB plan to the 1TB plan cuts your per-GB rate by about 58%. That's a real discount if you have the volume to justify it.

Second, and this is the part people miss, the entry rate is roughly 50% higher than the headline number. Oxylabs' own marketing mentions residential proxies "starting from $4/GB", and that rate does exist, but it's attached to the $500/month Advanced tier. On the smallest self-serve plan it works out to $6/GB.

Plan names have moved around before, too. The plan now called Corporate was previously named Premium, and before that the per-GB rates on comparable tiers were $8 to $15. So the ladder you see in a review from two years ago is not the ladder you'll see at checkout today.

## Where the pricing gets awkward

Three structural details matter more than the sticker rate.

**Unused traffic.** Monthly tier plans are commitments, not wallets. Third-party comparisons list Oxylabs' unused bandwidth as expiring with the billing cycle. If that's a dealbreaker for your workflow, confirm it with their support before you buy, because it changes the math completely for sporadic scraping jobs.

**Tier gaps.** If you need 150GB in a month, you're buying the 125GB tier and topping up, or jumping to a custom arrangement. There's no self-serve 150GB plan. For teams whose volume swings month to month, that means either overbuying the next tier up or paying per-GB overage rates.

**VAT and extra charges.** Oxylabs' product pages note that VAT may apply depending on where you are. The listed $30, $100 and $500 figures are pre-tax for many buyers, which is a 20%-ish difference in Europe and similar elsewhere.

None of this makes Oxylabs bad value. It makes it a product designed for teams with steady, forecastable, high-volume workloads. If that's you, $2.50/GB at 1TB is competitive with anything in the premium tier.

## Oxylabs pricing beyond residential

Residential gets all the attention, but a lot of "oxylabs pricing" confusion comes from the fact that the other products bill on completely different units.

| Product | Billing unit | Reported entry point |
| --- | --- | --- |
| Residential proxies | per GB | $30 for 5GB ($6/GB) |
| Shared datacenter | per GB | roughly $0.44 to $0.50/GB |
| Dedicated datacenter | per IP per month | around $1/IP at 100 IPs, cheaper at 1,000 |
| ISP (static residential) | per IP per month | around $1.30/IP |
| Web Unblocker | per GB | ~$75 for 8GB, ~$325 for 25GB, ~$660 for 88GB |
| Scraper API | per successful result | reported tiers from ~$49/month (≈98k results) up to ~$2,000/month (≈8M results) |
| Headless Browser | per GB | $300/50GB, $550/100GB, $1,410/300GB, custom above 400GB |

Those per-IP and per-result figures are the ones that trip people up. Datacenter and ISP proxies are rented by IP, not by bandwidth, so a "cheap" $1/IP rate on 100 IPs is $100 a month whether you send one request or a million. The Scraper API flips it again: you pay per successful result, which makes budgeting predictable at scale but means the cost per 1,000 records varies with how difficult your targets are and whether JavaScript rendering is involved.

The rotating ISP line has its own ladder, quoted per GB but gated by IP count:

| Plan | IPs | Rate | Monthly |
| --- | --- | --- | --- |
| Starter | 340 | $17/GB | $340 |
| Business | 700 | $14/GB | $700 |
| Company | 1,100 | $11/GB | $1,100 |
| Enterprise | from 6,000 | custom | custom |

Oxylabs also mentions a 10% discount on annual plans for that product line, which is worth asking about if you're signing anything longer than a month.

One more note on the residential pool size: Oxylabs quotes different numbers on different pages, from "100M+" to "175M+" across 195 locations. Both are large. Treat the exact figure as marketing rather than a spec.

## The workload most people actually have

Here's the realistic scenario. You're a small team, or one developer with a scraping side project. You need 50GB to 150GB a month, sometimes less, sometimes a spike when a client asks for something urgent.

On Oxylabs residential, 100GB means the $500 Advanced tier, because the 20GB Basic plan won't cover it. You're paying $500 for a month in which you use 100GB. That's $5 per GB actually consumed at a listed rate of $4/GB. On a quiet month you use 40GB and still pay $500, because the commitment doesn't flex. That's $12.50 per GB of real usage.

This is exactly the gap pay-as-you-go per-GB pricing was built for.

## The alternative: pay only for the traffic you burn

DataImpulse runs the opposite model. No subscriptions, no monthly minimum, and traffic that never expires. You top up a balance and draw it down. Rates as published:

| Plan | Product and volume | Price | Billing | Buy |
| --- | --- | --- | --- | --- |
| Residential Intro | 5GB residential | $5 | One-time top-up, no expiry | Grab 5GB of residential traffic for $5 |
| Residential Basic | 5GB to under 1TB residential | $1/GB | Pay as you go, no expiry | Top up residential traffic at $1/GB |
| Residential Advanced | 1TB and above residential | $800/TB ($0.80/GB) | Bulk top-up, no expiry | Check the bulk residential rate at 1TB |
| Datacenter Intro | 10GB datacenter | $5 | One-time top-up, no expiry | Start datacenter traffic at $0.50/GB |
| Datacenter Basic | 100GB datacenter | $50 | Pay as you go, no expiry | Get 100GB of datacenter traffic for $50 |
| Datacenter Advanced | 1TB datacenter | $450 ($0.45/GB) | Bulk top-up, no expiry | See the 1TB datacenter pricing |
| Datacenter Custom | 5TB+ datacenter | from $2,250 | Custom quote | Ask about high-volume datacenter pricing |
| Mobile Intro | 2.5GB mobile | $5 | One-time top-up, no expiry | Test mobile proxies for $5 |
| Mobile Basic | 25GB mobile | $50 ($2/GB) | Pay as you go, no expiry | Buy 25GB of mobile traffic |
| Mobile Advanced | 1TB mobile | $1,600 ($1.60/GB) | Bulk top-up, no expiry | Check the 1TB mobile rate |
| Mobile Custom | 5TB+ mobile | from $8,000 | Custom quote | Request a mobile volume quote |
| Premium Residential Intro | 1GB premium residential | $5 | One-time top-up, no expiry | Try premium residential for $5 |
| Premium Residential Basic | 10GB premium residential | $50 ($5/GB) | Pay as you go, no expiry | Get 10GB of premium residential traffic |
| Premium Residential Custom | 5TB+ premium residential | from $20,000 | Custom quote | Discuss premium residential volume pricing |

The numbers to hold onto: **$1/GB residential, $0.50/GB datacenter, $2/GB mobile**, all pay-as-you-go with non-expiring traffic and a $5 minimum. Country targeting is included in the base rate; city, ZIP and ASN targeting is a paid add-on, and on standard residential plans that add-on is billed at a premium over the base rate, so factor that in if you need street-level precision rather than country-level.

The network is 90M+ IPs across 195 countries, with HTTP/HTTPS and SOCKS5 support and both rotating and sticky sessions. Intro plans carry a 7-day money-back guarantee for card payments as long as you've used less than 80% of the traffic.

Do the 100GB comparison again: Oxylabs Advanced tier, $500. DataImpulse at $1/GB, $100, and whatever you don't use stays in your account for next month. Same 100GB, one-fifth the cost. What you're giving up is scale of pool, an enterprise compliance stack, and the depth of the Scraper API and Web Unblocker products if you need managed unblocking rather than raw IPs.

That's the actual tradeoff. Oxylabs isn't overpriced for what it is; it's priced for a buyer with different requirements than most people typing "oxylabs pricing" into a search box.

## How to test before you commit to anything

1. Estimate your monthly volume, then add 30% for retries. Blocked requests still consume bandwidth.
2. Price both models against that number. A tier plan's effective rate is your total bill divided by gigabytes actually used, not the listed per-GB figure.
3. Buy the smallest possible package first. A $5 top-up tells you your real success rate on your own targets, which is the only number that matters for cost per useful request.
4. Check whether your targets need country-level or city-level targeting. Country-level is included at DataImpulse; city and ASN cost extra.
5. Scale only when cost per successful request beats your alternatives. A $1/GB pool that fails on your target is more expensive than a $4/GB pool that doesn't.

If step three sounds appealing, you can start with a single top-up and no subscription: 👉 start at $5 for 5GB of non-expiring residential traffic, then measure your own numbers before committing to a monthly tier anywhere.

## Questions people ask about Oxylabs pricing

**Does Oxylabs have a true pay-as-you-go plan?**
Yes, at roughly $8/GB standard, with a capped promotional rate around $4/GB. The catch is that it's the most expensive way to buy from Oxylabs, and the rate improves sharply only if you move into monthly tiers.

**What's the minimum spend?**
$30/month on the smallest self-serve residential plan, before VAT.

**Why is my bill higher than the per-GB rate suggests?**
Usually one of three reasons: your volume pushed you into a tier you don't fully use, VAT applies, or you added paid targeting or extra products.

**Are there discount codes?**
Oxylabs partner landing pages have carried codes offering 20% off the first month on selected residential plans, restricted to new customers and to the first subscription month. Read the conditions, because they typically don't apply to every tier.

**Is there anything cheaper without a monthly commitment?**
Yes. DataImpulse charges $1/GB residential with no subscription and no expiry on unused traffic, and 👉 the entry point is a single $5 top-up rather than a monthly contract.

## Bottom line

Oxylabs pricing rewards commitment. If you're pushing hundreds of gigabytes or more per month and you want the compliance paperwork, the managed unblocking stack and an account manager, the $2.50/GB you reach at the 1TB tier is a fair price for a premium network.

If you're the person who searched for "oxylabs pricing" because the checkout page surprised you, the tiered model is probably not built for your workload. A pay-as-you-go rate of $1 per gigabyte with traffic that doesn't expire keeps you from paying for gigabytes you never send. Same job, different bill.

Whichever way you go, the discipline is identical: measure cost per successful request on your own targets before you scale anything.
