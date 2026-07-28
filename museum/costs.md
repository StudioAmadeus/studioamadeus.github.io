[Essay](../) · [Log](../log/) · [The Quarterly Close](../almanac/) · [Museum](./)

# The measured-cost table

**In plain words:** what trading has actually cost, measured from each fill's own quote receipt — never estimated, never modeled after the fact. Costs are the quiet killer of most trading ideas, which is why this table is a standing exhibit rather than a footnote.

| book | fills | notional (USD) | paid (USD) | avg bps | cap bypasses |
|---|---|---|---|---|---|
| prob-fartcoin | 1 | 80.00 | -0.01 | -1.6 | 0 |
| prob-jlp | 1 | 80.00 | -0.01 | -1 | 0 |
| prob-jup | 1 | 80.00 | -0.03 | -4.3 | 0 |
| prob-pengu | 1 | 80.00 | -0.33 | -41 | 0 |
| prob-ray | 1 | 80.00 | -0.04 | -5.5 | 0 |
| rails | 1 | 87.59 | -0.02 | -2.2 | 0 |
| s0-rebal | 5 | 387.33 | -0.01 | -0.3 | 0 |
| s3-lite | 2 | 125.00 | 0.01 | 1 | 0 |
| **total** | 13 | 999.92 | -0.44 | -4.4 | 0 |

Measured from each FILL's own quote receipt: both legs valued in USD at the fill's mark, the gap being the quoted LP fee plus price impact actually paid. A negative total means the quoted route beat the mark used to value the legs — price improvement, recorded as-is. Paper mode charges no router or priority fee, and says so on every receipt (§5). Costs are facts, not verdicts — the referee already nets them.

---

*Compiled from the ledger's fill receipts by the press; re-rendered at boundaries and closes, never live.*
