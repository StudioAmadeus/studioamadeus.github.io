# We deleted 3,246 records from a machine that never deletes anything

The whole system runs on an append-only ledger. Nothing gets edited,
nothing gets removed. If something's wrong, you write a new entry saying
so. That rule is enforced by the database itself, and it's the closest
thing this project has to a religion.

Last week we deleted 3,246 records on purpose. I want to explain why
that's not a contradiction, because the reasoning matters more than the
number.

The machine collects data on new coin launches — an archive of every
launch it sees, snapshotted on a fixed clock, so that someday there's an
honest dataset that includes the dead ones. The first version of the
collector had a calibration bug. Wrong reference points, wrong crash
flags. The measurements it wrote weren't lies exactly, but they weren't
observations either. They were noise wearing a number.

And here's the line we drew. The ledger — the money record, the trades,
the rulings — never gets touched. Ever. That's evidence. But a
measurement that's been proven mislabeled isn't evidence. Keeping it
around doesn't make you honest, it makes your dataset quietly wrong
forever, and every summary computed over it inherits the wrongness.

So: honest observations never die. Proven-false ones don't get to
pretend to be history. We kept the proof of the bug, fixed the
calibration, purged the bad rows, and the collector started over
clean. It was about 6MB. The space was never the point. Coherence was.

— Adam, Studio Amadeus
