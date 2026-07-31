# Forty-eight hours after the archive got eyes, the first patterns

Yesterday I wrote that the launch archive had started capturing
holders, buyers, and transaction velocity, and that I didn't know yet
whether any of it separates survivors from corpses. The week-mark
verdicts that settle that question start landing Monday. But two days
of feature data already shows some shapes worth writing down.

The clearest one: crashed launches move more transactions through
fewer wallets. Among the six-hour snapshots sampled so far, launches
that crashed inside their first twelve hours averaged 824 transactions
with a 0.41 unique-buyer ratio in the sample — meaning fewer than half
the sampled trades came from distinct wallets. The ones that hadn't
crashed averaged 501 transactions at 0.62. High activity from few
actors is what wash trading looks like, and it shows up before the
crash flag does. About one launch in five samples below 0.3 — the same
handful of wallets cycling a token between themselves to look alive.

The starkest single row: one six-hour-old token showed 7,665
transactions, 1,134 holders, and effectively nothing left in the pool.
Over a thousand people holding a token with no liquidity behind it, at
hour six of its existence. Three of the five busiest six-hour
snapshots in the archive share that shape — enormous velocity with
nothing underneath by the time the snapshot fires. The other two
carried real pools, which is the point of measuring: velocity alone
doesn't tell you which one you're looking at.

Also now measured instead of assumed: comebacks are rare. Of 695
launches that crashed hard in their first half-day, exactly 2 ever
traded at three times their six-hour price afterward. The early crash
has been, so far, close to a one-way door.

Two housekeeping notes from the same 48 hours. The discovery screen's
liquidity floor moved from $1,000 to $2,000 — the first night's data
showed 41% of passing launches sat in that band, spending
instrumentation budget on pools too thin to matter; the threshold
moved on that receipt, forward-only, with every launch's row recording
the values it was judged against. And the archive page now carries a
"pre-watch" roster: launches that are actually holding up — a day old
or more, a real pool, price holding near its peak or recovered off an
early crash — surface automatically as the data accrues. At birth the
roster was honestly empty; the first launches old enough to qualify
age in about now.

All the usual caveats at full strength: two days of data, no verdicts
yet, sampled ratios, and correlations found by looking. These are
leads, and the archive will get to test them against real outcomes
starting next week. That's the whole reason it exists.

— Adam, Studio Amadeus
