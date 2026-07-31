# The generator hit a wall, and the wall went into the record

We upgraded the machine's hypothesis generator on July 29th, and the upgrade
started with a failure worth describing.

Every strategy idea the machine tests is generated blind — the generator
proposes a typed spec, never sees results, and the exact context it faced
gets hashed into the trial's registration. Until now we enforced the spec
format with a compiled grammar: the API itself forced the output shape.
The newest generation of models refuses that grammar outright. "Compiled
grammar is too large." Every call, same error, measured.

The builder recommended stepping back to an older model and told me the
newest large model didn't exist. I asked "what about Opus 5?" — and the
live model list proved it did. It rejected the same grammar anyway, which
turned out to be the useful result: the wall was the schema's size, and
no new-generation model was going to walk around it. The older models
accept the grammar fine; the frontier ones refuse it, and the frontier
is where we wanted to be.

So we measured the alternative before adopting it. Put the JSON schema
inside the prompt itself, ask the model to comply, validate on our side.
Bare, that path produced zero valid specs in three attempts — length caps
blown every time. With a hard length-limits instruction added, three for
three, on both frontier models we tested. That receipt made the decision:
the generator now runs on the most capable available model, with the
schema and the length limits riding inside the prompt — which means they
ride inside the manifest hash, so every trial still carries proof of the
exact grammar it faced.

One deliberate omission: there is no fallback model. If the model refuses
or garbles, that registers as a malformed trial and counts against the
ledger, honestly. A silent mid-batch switch to a backup model would
poison the record of what generated what, and the record outranks
convenience here.

The first real batch under the new generator ran on July 31st. Five
hypotheses, five distinct mechanism families, zero malformed, zero
invalid, zero duplicates — and then five funerals. Four of the five
survived all the way to the final holdout window before dying there,
which no earlier batch managed; the failure classes that used to be
about form — fragile parameter peaks, specs that never trigger — didn't
appear at all. The new generator writes better-built ideas. The market
still declined all of them, which is the gauntlet doing its job, and
the proof bar those five trials purchased now sits higher for the next
batch. Cost: about a dollar or two of API spend for the batch, in line
with the estimate that justified the upgrade.

— Adam, Studio Amadeus
