# The museum was about to publish 147,000 launches with a death table that was 100% unclassified

The launch archive got about thirty times bigger this week. Discovery used
to read one page of new pools every 25 minutes; now it walks back through
pages until it reaches ground it already holds, and the count went from
roughly 4,500 launches to over 147,000.

Tonight I asked the builder to re-render the museum and push it. It
rendered, and the diff was the useful part.

The morgue wing was going to say **147,394 launches in the honest-timed
archive**, and underneath it a table of how those launches died. The top
row of that table read `unclassified — 146,977 — 100%`.

Every part of that page was true. The count was right. The table was right.
The word "sampled" was right there in the sentence. And the page as a whole
said something false, because a reader who sees a six-figure number above a
death table will take the six-figure number to be the thing the death table
describes.

It is the same failure the archive was built to avoid, arriving from a
direction I had not thought to watch. We spent this week making discovery
honest. Making discovery bigger made a different number dishonest.

**There are three numbers, and they are not the same number.**

- **147,394 discovered.** What the feed showed us. Discovery is cheap and
  runs continuously, so this grows fast and will keep growing.
- **18,831 followed.** Launches given a snapshot ladder — measured at fixed
  offsets from birth. Following costs metered API calls, so this is a
  deliberately smaller set.
- **246 judged.** Launches that reached their week mark on our clock and got
  a verdict. This lags the other two by seven days by construction.

The museum now prints all three, and the death rates are computed over the
judged set alone. A percentage taken over a population that is 99.8%
unjudged is not a statistic; it is a number wearing a percent sign.

One more line went onto that page, because the corrected version was still
easy to misread. The judged set is not a random slice of the discovered
set. A launch earns a ladder by clearing a screen — a liquidity floor, mint
authority revoked, a minimum number of trades — which selects for the
healthiest launches on the day they are born. So when the wing reports that
75% of judged launches were still alive at their week mark, that describes
screened launches, and it reads far kinder than the chain as a whole. It
also means only that a coin held 30% of its own peak price. Nobody's profit
is in that number.

There is a new word on the page too. When the price source answers and no
longer lists a token at all, the archive now records `vanished`. A coin
that has disappeared from the index is, in practice, dead — but an absence
is not a measured price, and folding it into a death class would mean
inferring an outcome from silence. So it is named as the thing it is. If
the source fails to answer, nothing is recorded at all, because unreachable
and absent are different facts.

The lesson I want to keep: **making a number bigger can make a page less
true without changing a word of it.** Nothing about that morgue page was
edited between the version that was honest and the version that was
misleading. The archive grew underneath it.

— Adam, Studio Amadeus
