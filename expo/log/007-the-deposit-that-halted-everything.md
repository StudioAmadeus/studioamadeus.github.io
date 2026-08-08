# A $53 deposit halted the whole machine — and found two bugs doing it

I sent this week's deposit a couple of days early, just before
midnight. Two minutes after the money landed, the machine halted all
nine of its paper books and alerted my phone.

The fourth law was doing its job: the ledger's balances must equal
the chain's balances exactly, to the raw unit, and when they don't,
the machine assumes the worst and stops trading. The deposit made the
chain hold more than the ledger knew about, the check saw a mismatch,
and everything froze.

Two problems with that, and they're both more interesting than the
halt itself.

First: the check was blind to direction. Money *missing* from the
wallet is the real emergency — that's the shape of a stolen key. Money
*arriving* is not an emergency at all; someone gave us funds. Worse,
blockchain addresses aren't secrets — anyone who has ever traded with
a wallet, or just watched the chain, can send tokens to it, unasked.
Under the old rule, a stranger airdropping some worthless token would
have frozen all nine books until a human intervened. Our own code
comments had even named that scenario. We'd built a machine a stranger
could switch off with pocket change.

So the rule now reads direction before it reads size. A deficit —
chain below ledger, on any token we track — still halts everything,
loudly, exactly as before. A surplus in a token we can book gets
booked as a deposit, with a normal-priority note instead of a siren.
And unknown junk tokens are excluded from the invariant entirely: the
machine can't trade them, can't book them, and now can't be halted by
them. Trading against ledger balances while a surplus is being booked
is safe by construction — the machine believes it has less money than
the chain holds, never more.

Second, the better bug: the deposit was invisible. The machine polls
the wallet's transaction history to book deposits, and my deposit
simply wasn't in it — and never would have been. On Solana, a
token transfer into an *existing* token account never references the
owner's wallet address, so the wallet's own history doesn't contain
it. The first deposit ever was visible only because it happened to
create the token account. Every deposit after the first, for every
token, forever, would have been invisible to the old code. The weekly
deposit plan would have broken silently starting that night.

The fix is to walk each token account's history too, which is where
those transfers actually live.

Both fixes are tested, the halt was cleared by hand and logged, and
the incident stays in the ledger forever — the false alarm is part of
the record, receipts and all. The deposit itself booked fine, about
forty-five minutes late.

What I keep coming back to: the machine was paranoid in the wrong
direction, and the way we found out was by using it. Fifty-three
dollars bought two bug fixes that no amount of staring at the code had
found. Cheap.

— Adam, Studio Amadeus
