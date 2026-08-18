# ReLeaf homepage — asset list (v0.3)

**24 photo slots, down from 29.** The hero is no longer a photograph, so five slots
disappeared and one was added. Every ID maps to a dashed box in `index.html` — search
`data-shot="P-07"`. Replace the whole `<div class="ph" …>` with an `<img>`, keeping the
outer wrapper classes.

Changed since the last list:
- **P-01 is no longer the hero background.** It is now the first photograph on the page,
  in a 4:3 frame. Same shot, same importance, different crop.
- **P-03 / P-04 are a side-by-side pair**, not a drag-slider. Same brief.
- **P-20, P-27, P-28, P-29 are gone** — the chat avatars and hover-reveal cards went with
  the Brno-style elements I removed.
- **P-30 is new** — YesHealth, for the fifth changelog entry.

---

## Tier 0 — not a photograph, and it now outranks everything

### The Arduino soil log  ⚠ blocks the hero's credibility
The hero is a live instrument readout. Right now it replays a **placeholder** trace, and the
page says so in amber, on the front page, under the gauges. That admission is fine for a
prototype and fatal at judging.

- **What:** EC (or a salinity proxy) and temperature, timestamped. Raw CSV straight off the
  Arduino. A few hours is enough; a few days is better.
- **Why it matters more than any photo:** the entire hero is the claim "we measure soil and
  the light follows." With a real log, a judge dragging that slider is playing with *your
  data*. With a placeholder, the best visual on the wiki is a mock-up.
- **Where it goes:** one function, `autoTrace()`, marked in the script.
- You already have `od600_log_20260721_034533` and its successors. If an EC/temp log sits
  beside them, that is the file.

---

## Tier 1 — the four photographs that carry the page

### P-01 · Device in soil, dusk, LED glowing
Still the most important photograph on the wiki. It is the proof that the glowing thing at
the top of the page is a real object.
- **Where:** outdoors, in actual soil or a real bed. A pot on a bench reads as fake.
- **When:** the 20 minutes after sunset — sky still blue, LED clearly brighter than ambient.
  **This is the whole shot.** In daylight the green vanishes.
- **How:** low, close, device filling most of the frame. Now a **4:3 crop**, so compose
  tighter than you would for a banner.
- Lock exposure on the sky, not the LED, or the green blows out to white.
- Shoot 30 frames across the 20 minutes.

### P-02 · 陳惠雯, portrait  ⚠ also blocks copy
Circular avatar in the changelog. Face centred, room around it.
- Outdoors on her farm, soft light, shoulders-up.
- **Get her quote and the date of the visit in the same conversation.** Two slots on the page
  currently read "Needs the real quote" and "DATE NEEDED".
- Confirm she is happy for her name, face and words to be published.

### P-03 / P-04 · Chamber dark → chamber at 520 nm
Two frames side by side, **same locked-off tripod**, nothing moved but the light.
- Manual exposure, manual focus, manual white balance. If any one is on auto the pair won't
  match and the comparison collapses.
- Tight on the chamber so the green fills it.
- Square-ish crop now (they sit in a 2×2 grid).

### P-23 · Group photograph
- Whole team, one wide well-lit frame, faces readable at 1200 px.
- Lab or the September forum. Not a collage.
- Stand on a chair so back rows aren't hidden.
- **21:9 crop** — leave generous head and side room.

---

## Tier 2 — the device is real (6 shots)

### P-05 · Whole device on the bench, wide
Cables, clamps, tape, all of it. Do not tidy first. Standing height, ~45°. Square-ish crop.

### P-06 · A hand holding the TFF module
Someone's hand holding the hollow-fibre module toward the camera. Instant scale, which no
spec sheet gives you. Plain background, close.

### P-07 · Breadboard with a multimeter probe on it
**The highest-value photo after P-01.** Probe tip touching a rail, meter body in frame with a
reading visible. Macro-close. Says "we measured this" better than any figure.

### P-08 · Wiring loom mid-build
Messy, unstyled, half-finished. Photograph the state you'd normally be embarrassed by.

### P-09 · 3D printer mid-print, pinch-valve body
Through the window, nozzle in motion, partial part on the bed.

### P-10 · Device in soil outdoors, daylight, panel up
The daylight sibling to P-01 — shows the deployment context the dusk shot stylises.

---

## Tier 3 — the evidence ladder (5 shots)

Four of these depict work in progress. Shoot what exists; don't stage what doesn't.

### P-11 · Reporter run on the instrument
**Screenshot the software**, don't photograph the monitor. If only the physical plate exists,
shoot the 96-well plate sitting under the array instead.

### P-12 · Activity assay tubes in a rack
The α-ketobutyrate assay. A colour gradient across the rack is the shot. Backlit against a
window beats top-lit.

### P-13 · Permeate vessel + a blank agar plate
The containment control. **An empty plate is a result** — label it in frame with tape and
marker so it reads as deliberate.

### P-14 · Seedling trays under salt stress
Trays side by side, ruler in frame, shot straight down. Even trays merely *set up* is honest
and better than an empty box.

### P-15 · SCREENSHOT, not a photo
Three-week OD600 trace, pump-death event marked with an arrow and a date. Export at 2×. Axis
labels and units visible.

---

## Tier 4 — what we killed (4 shots)

### P-16 · Gel of the verified ACCD construct
Straight-on, evenly lit, ladder visible. Screenshot from the imager if you have one.

### P-17 · A failure, photographed on purpose
The failed LEA14 transformation plate, or the blank gel lane. Most teams delete these.

### P-18 · SCREENSHOT: 5GR8 structure
Asn23–Arg487 contact highlighted, everything else desaturated. White background, distance
labels visible.

### P-19 · Whiteboard with the go / no-go decision
Real handwriting, real date in the corner. If it's been wiped, re-write it and **say so in
the caption** — don't pass a reconstruction off as the original.

---

## Tier 5 — the changelog portraits (3 shots)

Small circular crops, faces centred, shoulders-up. These give the Human Practices section
its authority: named people, dated, with the spec line each one moved.

- **P-21 · Dr. Pak K. Yuet** — used twice; two of his quotes are load-bearing.
- **P-22 · Instructors** — the "we NEED a 2nd safety net" line. A candid at a meeting is fine.
- **P-30 · YesHealth 源鮮農業** — NEW. Portrait of whoever you met, or their logo if no photo.
  **Also needs their quote and the visit date** (two more `data-fill` slots).

Anyone whose face and words appear here must have agreed to both.

---

## Tier 6 — the tail (3 slots, mostly not photography)

- **P-24 · Individual portraits** — already exist in `Wiki_member/assets/img/members/` at
  720×900. Reuse them, no shoot needed.
- **P-25 · DIAGRAM, make don't shoot** — one device → one row → one field, three gates
  labelled. Flat, simple, no 3D, no render.
- **P-26 · Project video** — embed from video.igem.org. A still frame with a play button
  until it exists.

---

## Shoot order — one afternoon and one evening

**Afternoon, in the lab:** P-07, P-08, P-05, P-06, P-16, P-17, P-12, P-13, P-09, P-21, P-22
**Late afternoon, outdoors:** P-10, P-14
**The 20 minutes after sunset:** P-03, P-04, then **P-01 last** — by then your exposure is
dialled and you're shooting the most important frame with practice behind you
**Separate trip:** P-02, her quote, and the farm
**Separate trip:** P-30, and the YesHealth quote
**At a desk:** P-11, P-15, P-18, P-25

---

## Things not to shoot

- People posing in a line holding equipment. Anyone giving a thumbs up.
- Screens photographed at an angle — screenshot instead.
- **A CAD render of anything.** Judges read renders as "not built."
- A tidied bench. The mess is the evidence.

## Handling

- Shoot the largest your phone offers. Hero and group: **2400 px** long edge; cards fine at 1200 px.
- Convert to `.webp` before upload — roughly halves the weight, and all four reference wikis do it.
- Everything must land on `static.igem.wiki`; the wiki blocks other hosts.
- Keep originals separate from uploads.

---

## Text still outstanding (6 `data-fill` slots)

| Slot | What |
|---|---|
| `quote-farm` · `date-farm` | 陳惠雯's actual objection, and the visit date |
| `quote-yh` · `date-yh` | YesHealth's constraint on permeate delivery, and the date |
| `team-n` · `school-n` | Team and school count — **three sources disagree.** The team-page README says 47 people, its design notes say 31 students, your blueprint says 32 students / 7 schools. The page reads 47 / 7 as a placeholder. Pick one. |

Also unresolved, and it is on the page in amber: the changelog entry for Dr. Pak carries the
line *"he recommended packed-bed; we chose hollow-fibre and owe the written justification."*
That is true — your own milestone map flags it as the highest-priority gap. A judge will ask.
Writing that decision matrix is worth more than any photograph on this list.

---

# Addendum · homepage v0.4 (18 Aug 2026)

The homepage was restructured around the instructor meeting's required element list.
Eight new slots, and a note on which old slots the new page no longer calls.

## New slots · P-31 to P-38

| ID | Where | What to shoot |
|---|---|---|
| **P-31** | Hero, lead frame | **The photograph the whole page rests on. Book a real shoot for this one.** A farmer we actually met, crouched at their own row, with the ReLeaf unit beside them **in the same frame**, its green light falling on their hands. Shoot at dusk so 520 nm is the only light source. The brief is one person, one machine, one picture: if the technology is visible without the person, the shot has failed. Not a portrait, not a product shot. Landscape 3:2, 2400 px. |
| **P-32** | Hero, support row | **A student.** One of us with hands on the reactor, mid-task. Real bench, real mess. No lab-coat portrait, no arms folded. Square crop. |
| **P-33** | Hero, support row | **The bioreactor.** Square and close, green LED lit through the fibre bundle. Square crop. |
| **P-34** | Hero, support row | **A leaf under real stress.** Roll, chlorosis or wilt. The damage has to read without a caption. A healthy plant here kills the argument. Square crop. |
| **P-35** | Problem 01 | **GIS stress map — a figure we generate, not a photo.** Our study region shaded by predicted heat and drought stress, with the farms we visited marked. Flat cartography, our palette, mono legend. Method goes on the Model page. |
| **P-36** | Solution | **Annotated bioreactor diagram — drawn, not rendered.** Sensor in, controller, LED array, culture chamber, hollow-fibre module, permeate out. Flat 2D. No 3D render (judges read renders as "not built"). |
| **P-37** | Human practices | **Expert and forum portraits.** Round crops for the changelog: Dr. Verslues, Prof. Cheng, Prof. Huang, plus one wide shot of the public forum showing actual attendance. |
| **P-38** | Human practices | **Field and facility visits.** CH Biotech and 源鮮 YesHealth. Show the storage or application step we were told about, not a group photo at reception. |

## Slots the v0.4 page no longer calls

`P-01`, `P-05` to `P-20`, `P-22`, `P-27` to `P-30` are not referenced by the new homepage.
They are not cancelled: the restructure moved hardware, results and process detail onto the
Hardware, Engineering and Measurement pages, where those shots belong. `P-02`, `P-03`, `P-04`,
`P-21`, `P-23`, `P-24`, `P-25`, `P-26` are still on the homepage.

## Text still outstanding on v0.4 (amber on the page)

| Slot | What |
|---|---|
| `quote-farm` · `date-farm` | 陳惠雯's actual objection, and the visit date |
| `quote-verslues` · `date-verslues` | Dr. Verslues on what counts as a real stress phenotype, plus the spec line it moved |
| `quote-experts` · `date-experts` | Prof. Cheng and Prof. Huang. **Split into two entries.** Do not merge two experts into one voice. |
| `quote-visits` · `date-visits` | CH Biotech and YesHealth, in the operator's own words. Record which deployment unit each site validated: per-plot, per-line, or racked. |
| `quote-forum` · `date-forum` | The forum objection we did not expect, and what changed because of it. If nothing changed, say so and say why. |

Numbers still owed, also amber on the page: membrane cutoff, cost per unit from a real BOM,
and confirmation of the contained-use classification from a Taiwan regulator rather than from us.

---

# Addendum 2 · homepage v0.5 "THE TURN (輪)" (18 Aug 2026)

The dark instrument build was replaced. The page is now a **work ledger**: a pre-printed
form on olive drying-yard concrete. Warmth is produced by type, colour, rules and the seal
rule, so it does not depend on photographs landing. That is deliberate: every slot below can
stay empty for weeks without the page looking broken.

## Slots this build calls

| ID | Where | Note |
|---|---|---|
| **P-H1** | Hero, straw band | **Book this shoot before anything else.** See brief below. |
| **P-H2** | Hero, top right | The shelf the reactor lives on. Do not tidy the shelf. |
| P-03 | Ledger section | Perfusion reactor on the bench, mid-run. |
| P-21 | 輪 Human Practices | Dr. Pak K. Yuet. **Square crop, 72px.** |
| P-37 | 輪 Human Practices | Verslues / Cheng / Huang / forum. Square crops. |
| P-38 | 輪 Human Practices | CH Biotech · 源鮮 YesHealth site visits. |
| P-23, P-24 | Team | Square crops. |

**Every portrait is SQUARE, not round.** Round portraits are Brno's signature and we are
deliberately not in that lane.

## P-H1 — the most important frame in the project

> Hands only, no faces. Two pairs of hands at the opened reactor on the workbench in the
> farm's tool shed: one older and calloused holding the fibre cartridge, one younger
> threading the M4 bolt. Diffuse daylight through the shed's translucent roof panel. Shot
> down the length of the bench so the spanner set stays in frame. The reactor is open.
> Nobody looks at the camera. Crop at the wrist.
>
> 35 mm · f/2.8 · available light · no flash · 40 frames

If it comes back staged (clean hands, tidied shelf, a student's forearms standing in for a
farmer's) **reshoot rather than ship it.** A staged frame here turns the page's whole moral
claim into decoration.

## The drawing is a commissioned asset, not a photo

The exploded reactor elevation in the hero is currently drawn in inline SVG and it is the
optical centre of the first screen. If a draughtsperson is available, book those hours.
**Hard fallback:** a single non-exploded orthographic section at the same size with the same
callouts. It must never become a blob with a green glow.

## Photo slots stay warm

Every slot renders as straw at 35% over the ground with a zinc dash, an index, the full
typeset brief and a spec line. This is what keeps the page warm before the shoot, and it is
the first thing that gets quietly dropped under time pressure. **It does not get dropped.**
