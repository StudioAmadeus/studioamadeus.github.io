# The machine told us it was fine. It was wrong four times.

Over the first week of August we rebuilt how the launch archive finds coins.
It used to poll one page of new pools every 25 minutes, which covered about
six percent of the timeline; now it walks back through pages until it
reaches ground it already holds. The archive went from roughly 4,500
launches to over 147,000.

That part worked. What follows is the part worth writing down: four separate
places where the machine reported success over a failure, and every one of
them was found by watching it run rather than by testing it.

**One: a retry that works hides the cost of the failure it recovered from.**
Snapshots were taking thirty-seven seconds each and nothing in the record
explained why. The data source was rate-limiting us, and our client
politely handled it — waited twenty-five seconds, tried again, succeeded.
Because the second attempt succeeded, no error was ever recorded. I could
query the archive for rate-limit failures and get zero, while more than
half the calls were being throttled. The only evidence was time that went
missing, which is the one thing none of our queries were looking at. We now
count the retries and publish them: the last few ticks read 45%, 61%, 56%,
44%, 50% throttled. Wider spacing and a shorter backoff took a snapshot
from thirty-seven seconds to about eleven.

**Two: a stop condition that could not tell "I finished" from "I ran out."**
The new discovery walk pages backwards until it reaches launches it already
has. Both "I reached covered ground" and "the source stopped serving me
rows" ended the loop, and the code treated them the same. So a walk that
gave up early reported a clean census while leaving a twelve-minute hole in
the record. Only reaching covered ground counts as coverage now; every other
way of stopping is named in the log along with how far back the walk
actually got. That change immediately told us something we had been
guessing at — the source only remembers about six minutes of new pools, so
discovery has to run more often than that or it cannot be contiguous at all.

**Three: a surface that counted its own failures as data.** The archive
schedules a snapshot at each rung of a ladder, and records a gap when it
misses one — deliberately, because the gaps are part of the record. The
console's ladder display counted every *resolved* row as an observation,
and a gap is resolved. At the launch-moment rung it showed every one of
18,725 resolved rows as an observation when 11,443 of them were misses.
Readings and gaps are counted separately now, and the corrected display
explains itself: two rungs sit far below the rest because they carry
thousands of scheduled snapshots for coins we later decided to stop
following.

**Four: a count that reported intent instead of outcome.** Each tick logged
"40 snapshot(s) captured." It was printing how many rows it had *selected*.
On ticks that captured four, it said forty.

The pattern is the same in all four. Nobody wrote a line of code that lied.
Each report was shaped like success because the failure had been handled,
or absorbed, or counted in the wrong column — and a handled failure leaves
no trace unless you deliberately make it leave one. A system that reports on
itself will flatter itself by default. It has to be made to count what it
missed.

That is the same lesson as the fact-check post in July, arriving from the
other direction. There, prose written by a human had drifted from the
receipts. Here, the receipts themselves were the problem: they were being
compiled honestly from measurements that had quietly stopped being
measurements of what we thought.

Two things are still open, and it would be dishonest to end without them.
The rate limiting is not solved — we are still throttled on roughly half of
those calls, and it caps how closely any one coin can be followed. And the
archive's ladder, counted over its whole life, is **78% gaps**: the period
before these fixes cannot be repaired, and it was worse than I would have
guessed before the display started telling the truth about it. Gaps are
never backfilled here. The record keeps its holes and says so.

— Adam, Studio Amadeus
