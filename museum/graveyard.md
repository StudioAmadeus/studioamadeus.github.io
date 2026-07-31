# The graveyard hall

**In plain words:** every trading idea this machine has tested and killed, on the record forever. Each was generated blind, locked with a fingerprint before any test ran, and judged by deterministic code against a bar that only rises. Dead ideas are the one cargo that always crosses the publication boundary — the living roster never renders here.

19 dead trials. The registry stamps registration; the gauntlet judges at the door, so each date below is both.

## #2 — Panic-Selloff Snapback Reversion

Family `mean_reversion` · died of **negative-evidence** · registered & judged 2026-07-17 · manifest `2f00045d8147…` · spec `e3347d7c321e…`

Cause of death, verbatim from the verdict: working set: Sharpe -0.29 ≤ 0

> Leveraged SOL longs get margin-called during sharp drawdowns, forcing indiscriminate selling that pushes price well below its short-term average faster than fundamentals justify. Once forced liquidation flow exhausts, price mean-reverts as panic subsides and opportunistic buyers step in. The counterparty paying for this edge is the panicked seller who dumps near the local bottom to meet margin calls or stop losses, plus momentum chasers who shorted the breakdown right before the snapback.

## #3 — Volatility Contraction Expansion Trend

Family `volatility` · died of **fragile-peak** · registered & judged 2026-07-17 · manifest `b643c17ece19…` · spec `974b38c58134…`

Cause of death, verbatim from the verdict: fragile peak: a ±20% parameter variant flips Sharpe non-positive

> When realized volatility compresses to multi-week lows, it signals a regime of low participation and indecision where market makers and short-vol carry traders accumulate one-sided inventory. Once price breaks out of this compressed range with rising vol, those inventory-heavy participants must chase or hedge in the direction of the move, creating a self-reinforcing trend leg. The edge exists because vol compression is a public, mechanical signal that most trend followers ignore (they filter for entries, not for regime), so the first movers after a squeeze capture drift that latecomers pay for via slippage and chasing.

## #4 — Volatility Regime Momentum Filter

Family `volatility` · died of **negative-evidence** · registered & judged 2026-07-17 · manifest `cd059c950f57…` · spec `a0a8e05e3666…`

Cause of death, verbatim from the verdict: working set: zero trades — spec never triggers

> When realized volatility is elevated (above its recent norm), it typically follows large directional moves driven by forced deleveraging or panic buying/selling that has informational content — trend continuation is more reliable in these regimes because participants are trading on genuine repricing rather than noise. Conversely, in low-vol regimes, price drift is mostly noise and mean-reverts. This strategy only takes trend positions (price above a moderate-term SMA) when realized vol is elevated relative to its own longer-term baseline, filtering out the chop-driven false signals that occur when vol is low and directional bets are more likely to be noise trades that get run over by the next reversal. The counterparty is momentum chasers in low-vol regimes who get faked out, and vol-blind trend followers who don't condition on regime and thus enter trades during periods when the signal-to-noise ratio is poor.

## #5 — Dual EMA Trend Persistence with Secular Filter

Family `trend` · died of **negative-evidence** · registered & judged 2026-07-17 · manifest `4f44d8b7a79b…` · spec `91ba33e31a8b…`

Cause of death, verbatim from the verdict: working set: Sharpe -1.04 ≤ 0

> Retail and even many systematic SOL holders anchor to recent price history and adjust position sizing slowly as the medium-term trend shifts. When the fast EMA(10) crosses above the slower EMA(50), it marks a genuine change in the balance of buying vs selling pressure, but because information diffuses slowly through a fragmented, retail-heavy holder base, price continues drifting in the new direction for weeks as latecomers rotate in. The SMA(200) regime filter ensures we only harvest this drift in a secular uptrend, avoiding false trend signals during structural bear markets where dead-cat bounces trigger the EMA cross but fail to persist. The other side of the trade is holders who exit too early on the initial cross-down noise, and short-term mean-reversion traders who fade the breakout only to be run over by continued momentum.

## #6 — Donchian Breakout with Trend Confirmation

Family `breakout` · died of **fee-killed** · registered & judged 2026-07-17 · manifest `453912307882…` · spec `3ceca6345e12…`

Cause of death, verbatim from the verdict: working set: Sharpe -3.14 ≤ 0

*The registry holds this trial's mechanism story, but its vocabulary does not clear the publication gate verbatim — the story is withheld, never rewritten. The epitaph above stands.*

## #7 — Capitulation Volatility Spike Reversion

Family `mean_reversion` · died of **negative-evidence** · registered & judged 2026-07-17 · manifest `f5cba2cc25ea…` · spec `f576716b9a8b…`

Cause of death, verbatim from the verdict: working set: zero trades — spec never triggers

> Sudden spikes in realized volatility on SOL/USDC typically coincide with forced liquidations and margin-call cascades rather than new fundamental information. During these spikes, sellers are price-insensitive (liquidation engines, stop cascades), pushing price below fair value. Once the cascade exhausts and price reclaims a short-term EMA, the overshoot corrects as buyers who avoided the panic step in, while remaining panic sellers have already been flushed out. The edge is paid for by forced/impatient sellers during the vol spike and captured by patient capital re-entering after confirmation of stabilization.

## #8 — Multi-Month Momentum Drift Continuation

Family `trend` · died of **bar-killed** · registered & judged 2026-07-17 · manifest `fb6e5fca91de…` · spec `9205fd339a3c…`

Cause of death, verbatim from the verdict: lockbox: Sharpe 0.41 below bar 0.46 (bench 0, formula 0.46)

*The registry holds this trial's mechanism story, but its vocabulary does not clear the publication gate verbatim — the story is withheld, never rewritten. The epitaph above stands.*

## #9 — Calm Regime Trend Persistence

Family `volatility` · died of **fee-killed** · registered & judged 2026-07-17 · manifest `5eab009ce8a9…` · spec `84c9de4537a2…`

Cause of death, verbatim from the verdict: working set: Sharpe -0.34 ≤ 0

> Realized volatility on SOL/USDC clusters: calm, low-vol stretches tend to coincide with steady accumulation and orderly trend continuation, while vol spikes mark forced deleveraging, margin calls, and panic that inject noise and mean-reversion into price. The edge is a volatility risk-premium harvest: staying long only when the market is both trending (price above a medium-term EMA) and quiet (realized vol below a modest threshold) avoids the chop and slippage-heavy regimes where fast money and leveraged traders are stopped out or forced to unwind. The counterparty is impatient leveraged traders and panic sellers whose liquidations spike vol and whose exit flow this strategy sits out of, re-entering only once conditions normalize.

## #10 — Momentum Acceleration Crossover

Family `trend` · died of **fragile-peak** · registered & judged 2026-07-17 · manifest `1654bbd087d3…` · spec `040fd7ac49de…`

Cause of death, verbatim from the verdict: fragile peak: a ±20% parameter variant flips Sharpe non-positive

*The registry holds this trial's mechanism story, but its vocabulary does not clear the publication gate verbatim — the story is withheld, never rewritten. The epitaph above stands.*

## #11 — Cross-Asset Donchian Breakout Breadth

Family `breadth` · died of **bar-killed** · registered & judged 2026-07-24 · manifest `76d67301364f…` · spec `0cc33ba0fda4…`

Cause of death, verbatim from the verdict: lockbox: Sharpe 0 below bar 0.51 (bench 0, formula 0.51)

*The registry holds this trial's mechanism story, but its vocabulary does not clear the publication gate verbatim — the story is withheld, never rewritten. The epitaph above stands.*

## #12 — Fear-Buying Trend Compliance Long

Family `discipline_gated` · died of **fragile-peak** · registered & judged 2026-07-24 · manifest `28f33600f635…` · spec `1ec974e0f0dc…`

Cause of death, verbatim from the verdict: fragile peak: a ±20% parameter variant flips Sharpe non-positive

*The registry holds this trial's mechanism story, but its vocabulary does not clear the publication gate verbatim — the story is withheld, never rewritten. The epitaph above stands.*

## #13 — Calm-Regime Volatility Persistence Long (Daily)

Family `volatility` · died of **fragile-peak** · registered & judged 2026-07-24 · manifest `0ad025ec4a91…` · spec `300876838c09…`

Cause of death, verbatim from the verdict: fragile peak: a ±20% parameter variant flips Sharpe non-positive

*The registry holds this trial's mechanism story, but its vocabulary does not clear the publication gate verbatim — the story is withheld, never rewritten. The epitaph above stands.*

## #14 — Multi-Month Momentum Threshold with Vol-Gated Entry

Family `trend` · died of **bar-killed** · registered & judged 2026-07-24 · manifest `5fc9fd082739…` · spec `8f1ed1cab676…`

Cause of death, verbatim from the verdict: lockbox: Sharpe 0 below bar 0.51 (bench 0, formula 0.51)

> Slow diffusion of fundamental information (adoption curves, institutional flows, macro narrative shifts) generates multi-month price drift that persists longer than efficient-market priors suggest. Retail and slow-moving allocators underreact to the initial move, then chase it late, paying the toll to those already positioned. The prior EMA-crossover variant of this family came within a hair of clearing its bar (Sharpe 0.41 vs 0.46) but likely bled edge to whipsaw entries taken during noisy vol spikes that mimic trend starts. This variant swaps the crossover trigger for a magnitude threshold on 90-day rate of change (a genuine multi-month drift confirmation rather than a noisy short-lag cross) and adds a realized-vol gate that blocks new entries when the market is in a turbulent regime, since chaotic vol is exactly where false momentum signals cluster and whipsaws are paid for. The mechanism and edge source are unchanged from the close-miss cousin; only the entry precision and risk gating are sharpened.

## #15 — Calm Breakout Momentum Conjunction (4h)

Family `vigilance_conjunction` · died of **fee-killed** · registered & judged 2026-07-24 · manifest `33463010004e…` · spec `60db8a4a7abf…`

Cause of death, verbatim from the verdict: working set: Sharpe -2.06 ≤ 0

*The registry holds this trial's mechanism story, but its vocabulary does not clear the publication gate verbatim — the story is withheld, never rewritten. The epitaph above stands.*

## #16 — Participation-Confirmed Range Escape with Trailing Ride

Family `breakout` · died of **bar-killed** · registered & judged 2026-07-31 · manifest `1dcc17872198…` · spec `af6803762aef…`

Cause of death, verbatim from the verdict: lockbox: Sharpe -2.76 below bar 0.54 (bench 0, formula 0.54)

*The registry holds this trial's mechanism story, but its vocabulary does not clear the publication gate verbatim — the story is withheld, never rewritten. The epitaph above stands.*

## #17 — Breadth-Held Multi-Month Momentum with Trailing Ride

Family `trend` · died of **bar-killed** · registered & judged 2026-07-31 · manifest `5c81d5d5b9eb…` · spec `bce2cac42d43…`

Cause of death, verbatim from the verdict: lockbox: Sharpe 0 below bar 0.54 (bench 0, formula 0.54)

> Multi-month momentum in crypto majors comes from staged capital arrival: allocators, treasuries, and retail waves enter over weeks-to-months after a regime turn, so 4-6 month strength continues on average. The other side is the anchored crowd that sold early into strength and the underreacting holders who wait for 'confirmation' that arrives only after most of the move. This family is LIVE in the graveyard: the first variant was sign-stable at lockbox 0.41 and both kills sat FLAT through falling windows under a bare long-flat vocabulary. This variant fixes exactly that: entry is a strong 120-day momentum threshold (roc(120)>0.10) above a secular sma(200) filter, but the position is MANAGED — a 25% trailing stop on closes converts a regime rollover into a defined giveback instead of an abandoned round trip, and re-entry waits for a fresh signal reset. Applied equal-weight across seven majors with 4-5y daily depth so the verdict reflects the mechanism, not one chart. Daily cadence with multi-month lookbacks keeps trade count low enough that the fee toll is a rounding error per holding period.

## #18 — Capitulation-Volume Dip Conjunction in Secular Uptrend

Family `vigilance_conjunction` · died of **negative-evidence** · registered & judged 2026-07-31 · manifest `2e7753fccc47…` · spec `f80d6580e25a…`

Cause of death, verbatim from the verdict: working set: Sharpe -0.19 ≤ 0

> The setup is a three-way conjunction that fires a handful of times per year per coin and never on a schedule: (1) a secular uptrend intact (price above the 200d average), (2) a sharp one-week selloff worse than -12%, and (3) dollar volume surging (up 80%+ over the same week) — meaning the drop is accompanied by real capitulation flow, not quiet drift. The sellers in that moment are forced and impatient: leveraged longs being liquidated and retail panic-exiting into a market whose long-horizon holders have not left. They pay the toll; the edge is showing up EVERY time this fires — at 3am, mid-holiday, during maximum fear — which discretionary traders systematically fail to do. The volume leg is what separates this from the buried quiet-dip spec: without participation, a dip is drift and we stay out. Once in, a 15% trailing stop off the highest close manages the position mechanically — small stopped losses when the knife keeps falling, long rides when the snapback extends into trend resumption. A cross below the 200d average force-flats regardless, so we never hold through regime failure.

## #19 — Euphoria-Abstinence Trend Hold

Family `discipline_gated` · died of **bar-killed** · registered & judged 2026-07-31 · manifest `46d912721616…` · spec `8e6a78e368a9…`

Cause of death, verbatim from the verdict: lockbox: Sharpe -1.55 below bar 0.54 (bench 0, formula 0.54)

> The rule is trivially simple and psychologically near-impossible: hold the secular uptrend, but stand flat whenever the market goes parabolic. When a major is up 50%+ in 30 days, social feeds, funding, and headlines all scream to add — and that is exactly when marginal buyers are FOMO retail providing exit liquidity to earlier holders. Blowoff phases have the worst forward risk/reward in crypto: continuation gains are modest while drawdown tails are catastrophic. A human who knows this rule still cannot sit out the most exciting week of the cycle; the machine can, every time. The edge is perfect compliance: capture the boring middle of the trend (price above the 150d mean, momentum positive but not parabolic) and cede the euphoric last leg in exchange for skipping the crash that regularly follows it. Costs are paid by euphoria buyers who enter at parabolic extremes and by disciplined-in-theory traders who abandon the rule exactly when it matters. Long/flat regime on daily bars keeps the fee toll trivial — a handful of state changes per year per coin.

## #20 — Banking-Week Flow Hold, Weekend Vacuum Abstinence

Family `structural_mechanical` · died of **bar-killed** · registered & judged 2026-07-31 · manifest `a8b62937c805…` · spec `b9d3871882ee…`

Cause of death, verbatim from the verdict: lockbox: Sharpe -1.88 below bar 0.54 (bench 0, formula 0.54)

*The registry holds this trial's mechanism story, but its vocabulary does not clear the publication gate verbatim — the story is withheld, never rewritten. The epitaph above stands.*

---

*Compiled from the registry by the press; re-rendered at boundaries and closes, never live.*
