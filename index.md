# My Trading Bot Has a Constitution

*Constitution as governance for an AI trading system.*

There's a trading strategy running on my laptop right now that no human wrote. An AI came up with it without ever seeing a backtest result. A pile of deterministic code it can't touch judged it against a bar that gets higher every time we search. I signed off on its admission the way a judge signs an order, and the whole thing went into a ledger I can't edit.

It's been flat for days. Hasn't traded once.

That's it working.

## Where I'm coming from

I run a kitchen for a living. And for a while there, I was a memecoin guy. The kind who's up at midnight refreshing a chart, telling himself he'll sell this time. I have the wallet history to prove it. I was actually good at the finding part — spotting the coin before it ran. It was everything after that killed me. Exits. Sizing. The tax bill I didn't plan for. If any of that sounds familiar, this post is for you.

Somewhere in the middle of all that I got into building software with AI, seriously, as a hobby. And eventually the two things collided into one question: could I use the AI skills to trade properly? Not "find me a 100x." Properly. Rules, records, receipts.

So I built a system called EXPO. It's named after the expo station in a kitchen, because the expeditor doesn't cook and doesn't write the menu. His whole job is making sure tickets go out right. That's the design philosophy in one job title.

Two Claudes run it with me. One is the planner — it lives in a chat, writes the plan, reviews everything, and argues with me when I'm wrong. The other is the builder — it lives in VS Code and writes all the code. I'm the director. Every judgment call, every risk number, every rule change goes through me, gets a number, and goes on the record. We're past sixty of those now.

And I'll just say the real point up front. Every exchange app on your phone was built by people who make money when you trade more. Everything I'm about to describe was built by a guy who needed to trade less. And needing it wasn't enough — I'd needed it for years. What I finally figured out is that discipline isn't a personality trait. You don't summon it at 2 a.m. You have to install it ahead of time, in daylight, as a rule you can't talk yourself out of. That's the whole project. Everything below exists to hold that one line.

## The problem with letting an AI trade

People keep wiring language models straight into exchanges. Last fall there was an experiment called Alpha Arena that gave six frontier AI models $10,000 each to trade crypto with nobody in the loop. Four of the six lost money — down four to six grand each — and the autopsy that stuck was pretty simple: transaction costs ate them alive, because the models traded way too much.

Sound familiar? It should. The machines failed the same way retail traders fail. Too many trades, costs ignored, conviction doing the position sizing. A language model is a brilliant analyst and a terrible trigger finger. So is almost everyone reading this. Which is why EXPO's first law got written before any other code existed:

**The AI never touches the money path.** Not once. Not in an emergency. Not "just this time." Signals, orders, fills — all deterministic code. The AI proposes, the machine executes, I approve.

## The constitution

That first law got siblings. They live in a document both AIs read every session, and most of them are enforced by code, not by anyone remembering:

**Everything is append-only.** The ledger literally can't be edited. The database rejects updates and deletes at the trigger level. If something's wrong, you add a new entry saying so — you don't make the old one disappear. When I deposited my first ten real dollars, the system booked it and then proved its books matched the blockchain down to the smallest unit. It keeps re-proving that, constantly. If the numbers ever disagree, it halts everything and screams at my phone. There's no version of this where a bad month quietly becomes "a learning experience" with no line items.

**Rules outrank strategies.** Position caps, daily loss breakers, a kill switch. They all live in versioned config that strategies can't even read, let alone change. Every trade records which version of the rules was in charge when it happened.

**Exits are never blocked.** We learned this one from a drill. There was a safety cap meant to stop bad fills, and it turned out that cap could block an emergency exit — meaning in a crash, the bot would've been trapped holding by its own seatbelt. We caught it in paper trading. It would have cost real money. Now it's law: a safety rail can stop you from getting in, but nothing is ever allowed to stop you from getting out.

**Elections, not polls.** Strategy settings get re-picked on a fixed schedule, like an election. Between elections, the math is free to complain that some other setting looks better lately. The complaint gets displayed, labeled ADVISORY, and ignored. You know this move — it's the strategy overhaul you talk yourself into after two red weeks. The rule kills it. (Funny enough, I had to amend this one myself. The first draft went too far and tried to ban even discussing the drift. Now the rule is: say anything, question everything, change things only through the process.)

## The strategy factory that mostly says no

The part I'm proudest of is called FORGE, and its main product is rejection.

An AI generates trading ideas blind. It gets the vocabulary it's allowed to build with, a description of the market data, and the graveyard of everything that already died. What it never gets is results — its ideas are locked in before any backtest runs, and every idea gets a fingerprint proving what the AI knew when it wrote it. Then deterministic code runs the gauntlet: out-of-sample tests, cost models built from fees we actually measured, sensitivity sweeps that kill fragile ideas, and a pass bar that rises with every attempt we've ever made. The more you search, the more proof the next idea owes you.

First batch: five ideas, four died, one made it. Second batch: five for five, all dead. One of those would have passed the first batch's bar — it died purely because the bar had gone up. Third batch: five more funerals, bar higher still. And every corpse teaches. Each dead idea becomes a constraint the AI reads before writing the next batch, tagged with its cause of death, so "we already know fees eat this" never has to be relearned.

Fifteen ideas in, one survivor on probation. That sounds like failure. It isn't. Most trading ideas don't work — that's just true — and the entire point of the factory is finding that out cheaply, on paper, before real money is anywhere near them. A ninety-three percent kill rate is what honesty looks like at scale.

The constitution also decided, ahead of time, what the factory is even allowed to want. Every corner of the market sits in exactly one declared state: hunted, watched, or dark — and dark patches need a signed ruling with a written wake-up condition. No unnamed blind spots. The most tempting dark patch, brand-new coins — my old vice — got its rules written before a single candidate exists. Any launch archive has to verifiably contain the dead coins before a backtest over it counts, because a dataset of survivors is a lottery ad, not evidence. And the dosage is already law: if that lane ever opens, positions run around one percent with mechanical exits, so a hundred-bagger doubles a book instead of becoming a life decision. The same concentration that mints a jackpot mints a zero. I've held both coins.

## The phone gets a bench, not a cockpit

Recently the dashboard grew a ruling surface, and its design rule is the whole constitution in miniature: **the console rules offers, never laws.** When the machine queues something up for me — a strategy earning a promotion, a new coin clearing the screens — my phone shows the exact event a tap would write, takes a passphrase, and signs it. Approve, decline, hold, a stake inside a pre-declared range. That's the entire vocabulary. Anything bigger doesn't even get a button. And every ruling instantly announces itself on the alert channel, including to me, so a stolen phone can't rule quietly. A few bad passphrases and the whole thing locks up and screams. The only way back in is at the keyboard.

The console's other founding law: **no casino mechanics, ever.** No confetti, no streaks, no dopamine flashes. And that's not a style preference — it's a build failure. There's an actual test that greps the stylesheet for celebration animations. Every exchange app on your phone was designed by people who profit when you trade more; this console was designed by someone who needed to trade less, and it took actual laws to hold that line. In the same spirit there's an 86 mode — kitchen slang made law. One passphrase halts all new entries across every book until I reverse it, while exits and circuit breakers keep working. The panic button only works in the safe direction. If you've ever deleted a trading app at 3 a.m. to save yourself from yourself, you already understand 86 mode. Except this one can't be reinstalled by a mood.

It even keeps a book on me. There's an optional one-question morning prediction, logged and scored against base rates. No money attached, ever. Most traders have never once seen their own hit rate. I get mine graded daily. It's humbling on purpose.

## What broke, and who caught it

Plenty broke. That's kind of the point of writing this.

We planned the whole deployment around a home server. During pre-flight, the builder swept my network to find it. It found a TV. The server didn't exist. The planner had assumed it from another project, I'd confirmed the assumption without checking, and nobody actually measured until the system's own rules forced it. The fix went in the changelog with names attached. Mostly the planner's.

The planner also broke its own rules twice in one day — dropped document updates mid-session where they got swept into unrelated commits, then violated a work-pacing limit it had written itself. Both times: named in the log, rule hardened, moved on. My favorite entry in the whole project is the audit that caught the system violating its own record-keeping law in the same document that announced the law.

Even an election got overturned. Turned out the first parameter vote had run under a mismodeled cost cap. The fix wasn't a quiet re-run. It was a formal amendment, argued on the record, executed as a signed event citing its own grounds, with the schedule clock reset from that day. The seat changed and the book didn't move a dollar. The win wasn't returns. It was that the pick and the model judging it finally agree.

None of this shook my confidence. Honestly, it built it. A system that catches its own authors is worth more than one that's never been tested.

## The honest part

Here's what the backtests actually say. The trend-following family I'm running on paper has negative out-of-sample returns over the last two years after real costs. The machine-discovered breakout is the one book with genuinely positive out-of-sample evidence — which is exactly why it's on probation instead of trusted. A third book got admitted with its confidence interval printed right in the admission record, and the record itself calls the margin "within noise." The system told me all of this plainly. I run the trend book anyway — small, capped, instrumented — because the first thirty days were never about profit. They're about proving the machine tells the truth under fire.

The dashboard is built to make lying to myself hard. Every performance number renders next to what just holding would've done, and that's a rule enforced by a test, not a habit. Returns show after a modeled tax hit, because active trading pays ordinary income rates, and if nobody's told you that yet, I'm telling you now, well before April. And there's one line on the chart the system can't massage: what a boring index did over the same window, pulled from an outside source, with its own honesty label (it's price-only, which actually understates the index). Once the weekly deposits start, that comparison becomes the full version — the same money, on the same schedule, held passively. The whole project gets judged by that line every day. If it can't beat the line, the line wins, and I'll say so in a follow-up post with the real numbers either way.

My planner told me on day one that it's skeptical the market will ever pay me, and confident the project already has. I asked it to stop hedging. It said that was the unhedged version. I kept the sentence.

The money involved is deliberately boring. I'm funding this fifty dollars a week out of a paycheck, and it goes live when the pile hits $250. Even that day is scripted — the wallet key gets its backup drill before anything arms, because the order of the ceremony was ruled in advance. Fifty a week is not a number that changes my life, and that's exactly the qualification it needed. If you came here hoping this ends with me quitting my job, wrong blog. The stream matters more than the strategies — the system's own math says so — and the strategies have to earn their way to touching it, one clean six-month review at a time.

## Steal it

The trading code stays private. The constitution doesn't.

I put the whole governance pattern in a [public template](https://github.com/StudioAmadeus/expo-constitution). The plan skeleton, the laws, the two AI role documents, the taste-call queue, the session logs. No strategies, no data. Just the operating system for pointing two AIs at something with real stakes without letting either of them — or yourself — quietly cheat. The machine also files its own quarterly report, called [The Quarterly Close](almanac/): what died, what it cost, where the bar sits now. It's free, it's receipts only, and the first issue comes out at the end of the year.

But you don't need the AI part, or even the bot part. If you're trading on vibes and promises to yourself — if you're who I used to be — steal the pattern bare. Write your rules down before the next trade. Keep a record you can't edit. Put your exits somewhere your feelings can't reach. Size positions so no single ticket can become a life event. Score your own predictions. A constitution is just a decision you make once, while you're sane, that keeps getting made when you're not.

If you're building anything where an AI's enthusiasm could cost you money, write it a constitution first. If your own enthusiasm is the expensive one, same instruction. The market is full of machines built to make you trade more. Build yourself the one that makes you trade less.

Mine mostly tells me no.

That's it working.

— Adam, Studio Amadeus

---

*If you found this interesting and want to buy me a coffee — or if this helped you and you want to pay it back — [here's the option](support).*
