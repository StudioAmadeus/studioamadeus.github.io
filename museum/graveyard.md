# The graveyard hall

**In plain words:** every trading idea this machine has tested and killed, on the record forever. Each was generated blind, locked with a fingerprint before any test ran, and judged by deterministic code against a bar that only rises. Dead ideas are the one cargo that always crosses the publication boundary — the living roster never renders here.

14 dead trials. The registry stamps registration; the gauntlet judges at the door, so each date below is both.

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

---

*Compiled from the registry by the press; re-rendered at boundaries and closes, never live.*
