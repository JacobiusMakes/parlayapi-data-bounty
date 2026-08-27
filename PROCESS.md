# Verification and Payout Process

> [!IMPORTANT]
> **Program status: NOT YET LIVE.** Launching pending founder sign-off. See the [README](README.md).

## Who verifies

The founder verifies every report personally. ParlayAPI is a small operation; that is a feature here, because the person confirming your report is the same person who can fix the bug and grant the credits.

## The steps

1. **Report filed.** You open an issue using the [data error report template](../../issues/new/choose). It gets the `unverified` label automatically.
2. **Archive check.** ParlayAPI continuously archives what the API served. The founder pulls the archived response for your timestamp and compares it against your screenshot and the eligibility rules in [RULES.md](RULES.md). The archive is the source of truth for what we served; your screenshot is the source of truth for what the book showed.
3. **Verdict posted in the issue.** One of:
   - `confirmed`: it is a real error and yours is the first distinct report. Root cause gets a short public writeup in the issue.
   - `duplicate`: real, but already reported or already in the resolution log. Linked to the original.
   - `not-an-error`: explained by movement, documented delay, or one of the other exclusions in RULES.md. The explanation is posted, not just the label.
   - `unverifiable`: missing required evidence. You can refile with complete evidence if the issue is still live in the data.
4. **Credit grant.** For confirmed reports, the founder grants 5,000 credits to your ParlayAPI account through the existing credit-grant flow (the same mechanism used for support adjustments). You will be asked in the issue thread for the email on your ParlayAPI account, or you can email it referencing the issue number if you prefer not to post it publicly. If you do not have an account, the free tier takes about a minute and requires no card.
5. **Resolution log entry.** Every confirmed report is added to [RESOLUTIONS.md](RESOLUTIONS.md) with the issue link, root cause, fix status, and reporter credit (GitHub handle, or "anonymous" on request). Rejected reports stay public in the issue tracker; we do not delete misses or disputes.

## Response targets

Solo founder, so honest numbers rather than enterprise theater: first response inside 3 business days, verdict inside 7. If a report ages past that, bump the thread.

## Transparency commitments

- The resolution log is append-only. Confirmed errors are never removed, including embarrassing ones.
- Verdict reasoning is posted publicly in every issue, including rejections.
- If the program is paused or ended, that goes in the README banner, and the log stays up.
