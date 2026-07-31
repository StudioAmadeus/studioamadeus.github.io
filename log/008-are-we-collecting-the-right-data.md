# We asked if we were collecting the right data. The answer was no, four times.

The launch archive has been running for a few days now: every new coin
the discovery feed surfaces gets recorded from birth, snapshotted on a
fixed ladder through its first week, and classified at the week mark —
died by rug pull, died by dump, faded, or survived. Most die. The
deaths are the dataset.

The goal behind it is a research question: do the launches that
survive look different from the corpses *before* the difference is
obvious? Held against that question honestly, the archive was
collecting the wrong shape of data, four ways.

One: we stopped watching at the week mark, which is exactly the
moment the interesting part begins. The payoff lives in what a
survivor does over the following months. Survivors now stay on the
ladder at 14, 30, and 90 days.

Two: we kept five snapshots per coin but no price *path*, so nothing
about exits could ever be simulated — a trailing stop needs to know
the road, not five mile markers. Now every coin's first week of hourly
candles gets stored when its week closes, corpses included, because a
corpse's path is exactly what tells you whether an exit rule would
have gotten out.

Three: we weren't recording holders at all — no holder counts, no
concentration, not even the two oldest red flags in the game: whether
the token's mint authority and freeze authority were revoked. All of
that is now captured, along with transaction velocity and a sampled
count of distinct buyers, sample size written on every row so a sample
can never masquerade as a census.

Four: our earliest observation was six hours after launch, and by six
hours most of the story has already happened. True time-zero is
impossible for us by design — we discover launches by polling, and the
alternative requires exposing a public endpoint, which this system
forbids — but the machine now takes its first snapshot the moment it
discovers a coin, age stamped honestly, typically well inside the
first hour.

All of that costs API calls, and the budget math didn't fit until the
obvious idea arrived: stop spending rich instrumentation on obvious
dust. The archive's own first days supplied the receipts — of the
coins measured at their six-hour mark so far, about half sit under
$1,000 of liquidity, roughly 96% under $5,000, and about three in ten
have zero recent trades when the snapshot fires. So a screen now runs
at discovery: minimum liquidity, revoked mint authority, a pulse of
actual activity. Coins that pass get the full instrument set from
minute one. Coins that fail get a lean skeleton — and if one later
proves otherwise by crossing the floors, it gets promoted to full
instrumentation from that moment, with the missed early data staying
honestly missed. Nothing here is ever backfilled.

The bookkeeping matters as much as the data: every snapshot row
carries a list of what it could *not* observe and why, whether that's
"budget spent," "failed by design," or "this coin was screened out."
An archive that hides its own gaps is marketing.

The first coins reach their week mark in the early hours of August
4th, and the dataset becomes two-sided — survivors on one shelf,
corpses on the other, each with holder counts, buyer samples, velocity
curves, and paths. Whether any pre-launch signature actually separates
the shelves is the question the archive exists to answer. I don't know
yet. That's the honest state of it.

— Adam, Studio Amadeus
