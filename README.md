# ParlayAPI Data-Accuracy Bounty

> [!IMPORTANT]
> **Program status: NOT YET LIVE.** This program launches pending founder sign-off. Until this banner is removed, reports are welcome but rewards are not yet being confirmed or paid out. Watch this repo for the launch.

Catch [ParlayAPI](https://parlay-api.com) serving a wrong line, earn free API credits.

We publish our misses because bettors should not trust a data vendor who hides them. Every odds API has errors sometimes: mapping bugs, stale feeds, book quirks. The question is whether the vendor tells you. This repo is our answer: a public, permanent log of every confirmed data error we have served, who caught it, and what we did about it.

## How it works

1. You spot a line in our API that does not match what the sportsbook's own app showed at the same timestamp.
2. You file a [data error report](../../issues/new/choose) with a screenshot, the timestamp, and our API response.
3. We check it against our internal capture archive.
4. If confirmed as the first report of a distinct issue, you earn **5,000 free API credits** (subject to founder confirmation and program continuation; credits only, no cash).
5. The issue and its root cause go into the public [resolution log](RESOLUTIONS.md), fixed or not.

Full eligibility rules: [RULES.md](RULES.md). How we verify and pay out: [PROCESS.md](PROCESS.md).

## Why we do this

ParlayAPI covers 30+ sportsbooks with live odds, player props, and historical data. Accuracy claims are cheap; every vendor makes them. Verifiable accuracy is not. We already publish open, reproducible latency and coverage comparisons in [odds-api-benchmarks](https://github.com/JacobiusMakes/odds-api-benchmarks). This bounty extends the same idea to correctness: instead of asking you to trust us, we pay you to prove us wrong.

If the resolution log stays short, that tells you something. If it grows, you will see exactly what broke and how fast we fixed it. Either way you know more than a marketing page would tell you.

## Quick links

- [RULES.md](RULES.md): what counts, what does not, evidence required, reward terms
- [PROCESS.md](PROCESS.md): verification and credit-grant flow, response targets
- [RESOLUTIONS.md](RESOLUTIONS.md): the public log of confirmed reports
- [File a report](../../issues/new/choose)
- [ParlayAPI docs](https://parlay-api.com/docs) and [pricing](https://parlay-api.com/pricing)
- [odds-api-benchmarks](https://github.com/JacobiusMakes/odds-api-benchmarks): open latency and coverage comparisons

## Not a bug bounty

This program covers data accuracy only. If you find a security issue in ParlayAPI, do not open a public issue here; contact us through the site instead.

---

Part of the [ParlayAPI](https://parlay-api.com) ecosystem: a real-time sports odds API with a free tier of 1,000 credits per month, no card required. Explore all the tools at [github.com/JacobiusMakes](https://github.com/JacobiusMakes).
