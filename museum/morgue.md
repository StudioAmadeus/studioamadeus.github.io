# The morgue

**In plain words:** the machine watches brand-new coin launches from birth on a fixed snapshot clock — not to trade them (that lane is dark by signed ruling), but to build the one dataset this genre never keeps: the launches that died, alongside the ones that lived. A dataset of survivors is a lottery ad, not evidence.

**What this is a sample of.** The machine watches the chain's new-pool feed. Until 2026-08-02 it read one page every 25 minutes, and a page covers about 1.4 minutes of creation time — so the launches below are roughly a **5-6% time-sliced sample** of everything that launched, against a measured rate of about 1,100 new pools an hour. It is a sample of *moments*, not of *winners*: whether a launch was observed does not depend on how it turned out, which is the property that makes the death rates below honest. From 2026-08-02 the feed is walked back to already-covered ground on every pass, so coverage is intended to be continuous — and the two periods are counted separately, because they are not the same population.

**Point-in-time honesty, stated as law:** every number is captured on its fixed offset or recorded as a gap — late measurements become gaps, never backfilled rows. **Survivorship disclosure:** this archive is everything seen since 2026-07-28; 26 rows are excluded as NOT LAUNCHES — established tokens that merely gained a new pool, which the discovery feed cannot tell apart from a birth and the archive now can.

**Three numbers, and they are not the same number.** **147,438** launches DISCOVERED · **18,847** FOLLOWED (given a snapshot ladder) · **246** JUDGED (aged a full week and classified). 1,560 crash-flagged so far.

Discovery is cheap and now runs continuously, so the first number is large and growing. Following a launch costs metered calls, so the second is a deliberately smaller set. A verdict needs a launch to survive to its week mark on our clock, so the third lags both by seven days. The death rates below are computed over the JUDGED set only — a share of a population that is almost entirely unjudged would not be a statistic.

**Read the rates as what they are.** The followed set is not a random slice of the discovered set: a launch earns a ladder by clearing the screen (liquidity floor, mint authority revoked, a minimum of trades), which selects for the healthiest launches on the day they are born. So a survival figure here describes SCREENED launches at their week mark, and it will read far kinder than the chain as a whole. "alive" means a launch held at least 30% of its own peak price — endurance, and no claim about whether anyone made money.

| death class | count | share of judged |
|---|---|---|
| alive | 185 | 75% |
| vanished | 46 | 19% |
| deployer_dump | 10 | 4% |
| lp_pull | 3 | 1% |
| fade | 2 | 1% |

Death classes stamp at launch+7 days over on-time snapshots only, so young cohorts sit unjudged until they age through the ladder — an honest lag, not a gap in the record. **`vanished`** means the price source answered and no longer lists the token at all: recorded as what it is, an absence, and never folded into a measured death class.

---

*Compiled from the launch archive by the press; re-rendered at boundaries and closes, never live.*
