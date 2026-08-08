# The rising bar

**In plain words:** the more ideas you test, the more likely one looks brilliant by pure luck — so the score every new idea must beat rises with every attempt ever made, and never comes back down. This is the machine's defense against fooling its own operator.

The formula, printed so it can never silently change: **bar = 0.30 + 0.15·ln(1 + N/5)**, where N is the lifetime count of trials ever registered (duplicates refused at the door never count). A live gauntlet judges at the HIGHER of this formula and the best passive benchmark's own held-out Sharpe.

<figure class="chart"><svg viewBox="0 0 640 200" role="img" aria-label="The pass bar over lifetime trials: 0.40, 0.46, 0.51, 0.54"><line x1="44" y1="166" x2="616" y2="166" stroke="var(--rule-strong, #b9ad96)" stroke-width="1"/><text x="44" y="182" font-size="11" fill="var(--ink-muted, #8a7f6c)">N = 0</text><text x="38" y="161.3" text-anchor="end" font-size="12.5" fill="var(--ink-muted, #8a7f6c)">0.30</text><path d="M 44.0 157.3 L 187.0 157.3 L 187.0 113.5 L 330.0 113.5 L 330.0 87.3 L 473.0 87.3 L 473.0 65.4 L 616.0 65.4 L 616.0 52.3" fill="none" stroke="var(--accent, #963c31)" stroke-width="2" stroke-linejoin="round"/><circle cx="187.0" cy="113.5" r="4.5" fill="var(--accent, #963c31)" stroke="var(--paper, #f7f3ea)" stroke-width="2"/><text x="187.0" y="103.5" text-anchor="middle" font-size="12.5" fill="var(--ink, #262119)" font-variant-numeric="tabular-nums">0.40</text><text x="187.0" y="182" text-anchor="middle" font-size="11" fill="var(--ink-muted, #8a7f6c)">batch 1</text><circle cx="330.0" cy="87.3" r="4.5" fill="var(--accent, #963c31)" stroke="var(--paper, #f7f3ea)" stroke-width="2"/><text x="330.0" y="77.3" text-anchor="middle" font-size="12.5" fill="var(--ink, #262119)" font-variant-numeric="tabular-nums">0.46</text><text x="330.0" y="182" text-anchor="middle" font-size="11" fill="var(--ink-muted, #8a7f6c)">batch 2</text><circle cx="473.0" cy="65.4" r="4.5" fill="var(--accent, #963c31)" stroke="var(--paper, #f7f3ea)" stroke-width="2"/><text x="473.0" y="55.4" text-anchor="middle" font-size="12.5" fill="var(--ink, #262119)" font-variant-numeric="tabular-nums">0.51</text><text x="473.0" y="182" text-anchor="middle" font-size="11" fill="var(--ink-muted, #8a7f6c)">batch 3</text><circle cx="616.0" cy="52.3" r="4.5" fill="var(--accent, #963c31)" stroke="var(--paper, #f7f3ea)" stroke-width="2"/><text x="616.0" y="42.3" text-anchor="middle" font-size="12.5" fill="var(--ink, #262119)" font-variant-numeric="tabular-nums">0.54</text><text x="616.0" y="182" text-anchor="middle" font-size="11" fill="var(--ink-muted, #8a7f6c)">batch 4</text></svg><figcaption>The pass bar over lifetime trials (N runs 0 → 20, left to right) — each step is a batch; the bar never comes back down.</figcaption></figure>

| batch | trials | lifetime N | bar at entry | bar after | died | survived |
|---|---|---|---|---|---|---|
| 1 | #1–#5 | 0 → 5 | 0.30 | 0.40 | 4 | 1 |
| 2 | #6–#10 | 5 → 10 | 0.40 | 0.46 | 5 | 0 |
| 3 | #11–#15 | 10 → 15 | 0.46 | 0.51 | 5 | 0 |
| 4 | #16–#20 | 15 → 20 | 0.51 | 0.54 | 5 | 0 |

The bar stands at **0.54** after 20 lifetime trials. Ideas have died purely because the bar rose between batches — that is the design working, not bad luck.

---

*Compiled from the registry by the press; re-rendered at boundaries and closes, never live.*
