# Bounty Rules

> [!IMPORTANT]
> **Program status: NOT YET LIVE.** Launching pending founder sign-off. See the [README](README.md).

## What counts as a data error

A report is eligible when ParlayAPI returned data that was wrong at the moment we returned it, compared against the sportsbook's own app or website at the same timestamp. Specifically:

1. **Price or point mismatch beyond the book's own movement.** Our API showed a price or line for a book that the book itself was not showing at that timestamp, and the difference cannot be explained by normal line movement between your two observations. Example: we return -110 on a spread the book had at -145 at the same minute.
2. **Wrong team, player, or event mapping.** We attached odds to the wrong team, the wrong player, the wrong game, or the wrong market. Example: a prop listed under the wrong player name, or home and away sides swapped.
3. **Stale data beyond our documented SLA.** A book we document as live or near-live returned odds older than our documented refresh interval for that book and market, and the book had moved in the meantime.

## What does not count

- **Books we document as delayed.** If our docs say a book or market updates on a delay, data inside that documented window is not an error.
- **Line movement between capture times.** Books move lines constantly. A difference explained by movement between when we captured and when you looked is not an error. This is why timestamps matter; see evidence requirements below.
- **Differences between a book's app and its website**, or between regional versions of the same book, when we correctly reflect one of them.
- **Markets or books we do not claim to cover.** Absence of data is a coverage question, not an accuracy error. Coverage requests are welcome as regular issues but are not bounty-eligible.
- **Errors in the book's own feed that we faithfully relayed**, when the book itself displayed the same wrong number.
- **Anything already in the [resolution log](RESOLUTIONS.md)** or already reported in an open issue. First distinct report only.
- **Errors you caused**: malformed requests, misread odds formats (decimal vs American), timezone mistakes in your comparison.

## Evidence required

Every report must include all three of the following. Reports missing any of them will be closed as unverifiable and are not eligible.

1. **Screenshot of the book's own app or website** showing the market and price, with the device clock or another timestamp visible or stated.
2. **Timestamp** of both your book observation and your API call, in UTC, as precise as you can make it. Within the same minute is the standard we verify against.
3. **Our API response**: the full request URL (mask your API key) and the relevant portion of the JSON response, including the response's own timestamp fields.

## Reward

- **5,000 free ParlayAPI credits** per first confirmed report of a distinct issue.
- Rewards are **subject to founder confirmation and program continuation**. Confirmation happens against our internal capture archive, not against the screenshot alone; see [PROCESS.md](PROCESS.md).
- **Credits only. No cash**, no gift cards, no equivalents. Credits are granted to a ParlayAPI account you control (the free tier requires no card, so anyone can receive them).
- One reward per distinct root cause. Ten reports of the same mapping bug across ten games is one issue.
- We may cap total program payouts or end the program at any time; the resolution log stays public regardless.

## Fair play

- No automated mass-filing. If you build tooling that finds real errors, we would love to see it, but file distinct root causes, not one issue per data point.
- Good-faith disputes about a rejection are welcome in the issue thread. Final call on confirmation rests with the founder.
