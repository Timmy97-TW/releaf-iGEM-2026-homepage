# What the homepage still needs

Prototype: `index.html`. Open it in a browser — no build step, no dependencies.
Every gap below corresponds to a visible slot in the page. Search the file for
`data-prov="verify"`, `data-prov="lit"`, and `class="slot"` to find them.

Ordered by **how much the homepage breaks without it**, not by how easy it is.

---

## Tier 1 — the page's central claim rests on these four

The hero number row and the transfer-function figure are the whole argument. Right
now three are empty and one is somebody else's data. Nothing else on this list
matters as much.

| # | What I need | Form | Currently |
|---|---|---|---|
| 1 | **Reporter dose–response.** Fluorescence vs. 520 nm intensity, ≥6 intensity points, n per point, error bars, and the intensity units you actually used | CSV or a table pasted into chat: `intensity, mean, sd, n` | empty slot, 8 circles drawn |
| 2 | **Your Hill fit** — n and K½ with confidence intervals, from *your* data in *B. subtilis* | two numbers + CI | showing Castillo-Hair 2019 |
| 3 | **ACCD activity.** α-ketobutyrate assay, P<sub>cpcG2-veg</sub> vs. constitutive P<sub>veg</sub> control | U/mg + n | empty slot |
| 4 | **Detect→deliver latency**, measured end to end | one number in hours + how you defined the endpoints | empty slot |

**On #2 specifically.** Your own 2026-07-04 spec freeze logs n = 1.88 ± 0.16 and
K½ = 4.66 ± 0.63 µmol m⁻² s⁻¹ as *Castillo-Hair 2019, E. coli, 526 nm*. The blueprint
is right that these must be your numbers. Until they are, the hero carries a blue
`lit` chip that says so out loud — which is survivable, but it is not the page you want.

**If the dose–response will not exist by October 4,** tell me now. The honest fallback is
to remove the hero number row entirely and lead on the hardware evidence (the three-week
log, the pump-death detection, the TMP instrumentation), which *is* measured and *is*
yours. A hero row of three dashes is worse than no hero row.

---

## Tier 2 — the hero animation

The animation currently runs on a synthetic signal. The blueprint requires real logged data,
and it's right: a judge who asks "is this your data?" and hears "no" loses the whole hero.

- **A soil sensor log** — EC (or salinity proxy) and temperature, timestamped, any length
  from a few hours up. Raw CSV from the Arduino is ideal; I'll decimate it.
- You already have `od600_log_20260721_034533` and its successors (93 → 223 KB across three
  weeks). If there's an EC/temp log alongside it, that's the one.
- Swap point is a single function: `driver()` in the hero script, marked with a comment.

**Fallback if no log exists:** one high-resolution photograph of the device soil-inserted,
outdoors, solar panel visible, replaces the animation entirely. **Not a CAD render** — judges
read renders as "not built."

---

## Tier 3 — photographs (5 slots, all empty)

Unglamorous is better than polished here.

1. **Bench build, wide** — the whole device on the table, cables and all.
2. **Breadboard with a multimeter probe on it.** This one does the most work of any photo
   on the page. It says "we measured this."
3. **A hand holding the TFF module** — instant scale.
4. **Device half-buried in soil**, outdoors, solar panel visible.
5. **The farm** — 陳惠雯's dew-mulch operation, for HP card #1. Must be real, not stock.
6. **Group photo** — one wide, well-lit frame. `Wiki_member/assets/img/group.jpg` exists at
   2400 px; tell me whether it's the right frame or whether there's a better one.

Any resolution — I'll crop and compress. For the iGEM wiki these need to end up on
`static.igem.wiki`; the team page README already covers that re-pointing.

---

## Tier 4 — Human Practices text

Three cards are drafted from what I could infer; the causal chains are guesses and
**must be replaced.** I could only find these visits in raw Discord JSON, not in any
written record.

For each of 陳惠雯 / 正瀚 / YesHealth I need three things:

- **Date** of the conversation
- **What we were going to build before it** — one sentence, concrete
- **What we build now** — one sentence, concrete, and it has to be a real change

The YesHealth card is the only one I could fill with confidence, because the constraint
it produced is in the spec freeze (permeate routes to the hydroponics reservoir first,
not to a single root; rhizosphere ring deferred). Confirm that's actually attributable
to YesHealth and not to something else.

The Sept 5 five-party forum card is stubbed and deliberately left empty. Fill it only
after the evidence is captured.

---

## Tier 5 — small factual gaps

- **Team size.** Three sources disagree: `Wiki_member/README.md` says 47 people,
  `notes/design.md` says 31 students, your blueprint says 32 students / 7 schools.
  Pick one, and give me the school count.
- **Device BOM total.** The milestone map flags this as missing and notes that every
  award writeup quotes a number (INSA <$400, UFMG $270, Cornell ~$300). You have none.
  Not on the homepage yet — but the "cost per device" gate in the big-picture diagram
  is currently an empty claim.
- **Second containment layer.** Called necessary on 2026-07-16, still no design. It's
  named as open on the homepage, which is the right call, but a judge will ask.
- **Real page URLs** for the footer six and every `href="#"`.
- **`inter-variable.ttf`** — inline it at bundle time for continuity with the team page.

---

## Things I deliberately did *not* do

- **No CAD renders anywhere.** The exploded view is a schematic, clearly diagrammatic,
  and it hands off to photographs immediately below. If you have CAD, it belongs on the
  Hardware page, not here.
- **No "blocks OMV" or protein-selective framing** of the membrane. Your own spec freeze
  records that claim as wrong. The page describes it as a cell-retention barrier and
  states that ACCD, small vesicles and debris all pass. This is falsifiable in one
  question at the poster, so it had to be right.
- **No "impressive for high schoolers" framing,** and no age signal above the roster line.
- **LEA14's kill reason is the one in your record,** not the one in the blueprint. The
  blueprint says "ruled out on structural grounds"; the 2026-08-13 status report says
  constructs G and H failed in *both* the light-driven and constitutive versions, which
  makes it a payload/junction failure. Those are different claims. I used the record's.
  If there's also a structural argument, send it and I'll merge them.
- **No problem/solution block, no superlatives, no parallax.**

---

## Word budget

The blueprint caps homepage prose at ~800 words. Running prose is currently **942**, plus
170 words of scaffolding that gets deleted at freeze (the "photo needed" captions and the
"what goes in this slot" notes). Spec strips, figure captions and labels aren't counted as
prose.

942 is over. The next 150 words to cut are in the figure captions and the rung
descriptions, and I'd rather you tell me which specificity is worth keeping than guess.
My view: the dated evidence (`2026-07-28`, `2026-06-10`, the OD600 numbers) is what makes
the page credible and should survive; the connective tissue around it can go.
