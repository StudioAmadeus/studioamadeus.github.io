# The machine rugged two of its own books by mistake

Just before 1 a.m. this morning, while I was asleep, the machine decided two of
its paper books were holding rugged coins. It sold both positions, froze
both books, recorded the demotions, and sent my phone the alerts. By the
rules, that's exactly what it's supposed to do when a token's liquidity
collapses below 15% of what it was at admission.

Except neither coin had rugged. Both were fine.

Here's what actually happened. Yesterday we ruled that the machine should
measure liquidity directly instead of relying on a screening list that goes
blind at the worst moment. Good rule. But the new measurement read the
reserve of one liquidity pool — the single busiest one — while the number
it was being compared against was the aggregate across all pools. For one
of the coins that came out as $56k against a $2.8M baseline. Fifteen
percent floor, breached, funeral.

The real aggregate, measured the same way as the baseline: $2.85M. Healthy.
The other book, same story at bigger numbers. And a third book was sitting
sixteen thousand dollars from the same false trigger.

So this morning went like this: disarm the bad measurements first —
the rule is built so a missing measurement never triggers anything, which
meant clearing five numbers made everything instantly safe. Then fix the
definition, re-measure all five coins, and verify them against their
baselines. Then, on my ruling, re-admit the two books with fresh baselines
and buy their positions back. The false alarms stay in the ledger forever,
because nothing gets deleted here — the mistake is now part of the record,
receipts and all.

Two things worth keeping from this. First: the definition is part of the
measurement. Two numbers with the same name and different definitions
aren't the same number, and comparing them isn't measuring. Second: the
rule's own safety design — evidence triggers, absence never does — is what
made the fix instant and calm instead of a scramble.

Paper money, real lesson. The go-live pile is glad we found this one now.

— Adam, Studio Amadeus
