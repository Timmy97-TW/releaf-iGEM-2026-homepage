# ReLeaf · project brief

*Paste this whole file at the start of any session, or hand it to a new teammate. It is
written to stand alone and assumes no prior conversation.*

**Version 2.** Version 1 was given to six readers who had no other context. All six invented
facts, in the same four places, because v1 asserted mechanisms in one section and retracted
them twenty lines later without saying which sentence won. Those contradictions are fixed
below, and everything the brief cannot supply is now listed explicitly at the end rather than
left as silence for a writer to fill.

---

## Who and where

GEMS Taiwan, a **high-school team**, competing in **iGEM 2026**, Biomanufacturing Village.
Deployment jurisdiction is **Taiwan**. Primary audience is iGEM judging; secondary audience is
farmers, instructors and collaborators. Pages are **English-first with 繁體中文 where a name,
a quote or a term is Chinese**; a farmer-facing artefact inverts that.

## The one sentence

**Every farmer a biomanufacturer.**

This is about **permission, not individual hardware ownership.** The economic unit is the
irrigation line and the owner is the cooperative. Wherever the headline and the economics
appear together, the reconciling sentence goes with them: *a farmer in a 產銷班 that owns a
reactor is a biomanufacturer in the only sense that matters, which is that no outside
licence-holder decides what gets made.*

## The vision

Biomanufacturing is gated. To obtain a useful protein you must buy it from somebody who owns
a fermenter, a cold chain and a registration dossier. None of the three is a scientific
obstacle, and none can be paid off across half a hectare. So smallholders are not served
badly; they are structurally not served at all, by arithmetic rather than by anyone's malice.

ReLeaf hands over the means of production: a bioreactor a farmer can build, own, repair and
retask, producing the protein their crop needs, where it is used, on the day it is needed.

## The position: say what we are not

- **Not climate change.** Climate is the weather the problem occurs in, not the problem.
- **Not farmer margins.** A few percent makes the project small and is not what is at stake.
- **Not hunger.** Hunger is mostly distribution and politics, not yield.

What is at stake is **who is permitted to manufacture.**

## The mission: what we are building

A perfusion hollow-fibre membrane bioreactor, small enough to sit where the crop is.

**Cost is a design target, not a result.** There is no bill-of-materials total, so no page,
headline or spoken pitch may use *cheap*, *low-cost*, *affordable*, or any per-unit price.

- **Two compartments, and use these words only.** Cells grow in the **extracapillary
  chamber**, outside the fibres. The **lumen** is the bore of the fibre. Without this
  vocabulary, "three weeks of OD600 logging" and "cells do not grow in the lumen" read as a
  flat contradiction. They are statements about different compartments.
- **Chassis.** Engineered *B. subtilis* 168, growing continuously in the chamber.
- **Control.** 520 nm light drives an optogenetic switch (CcaS/CcaR → P_cpcG2). Light
  intensity is intended to set transcription rate, so **brightness is dose** and the response
  is graded rather than switched. *Design intent, not a measured result. No induction curve
  exists in our hands.*
- **Latency.** Roughly **105 minutes to half-maximum**. **Borrowed, not ours**: published
  values from a different organism at a different wavelength. Any page using this number must
  say it is borrowed, in the same sentence, at the same type size.
- **Prediction.** A controller fuses a local sensor (soil moisture, EC, temperature) with an
  online weather forecast to call extreme heat, drought onset, and pathogen-favourable
  conditions before the plant shows them.
- **Containment.** The membrane is *intended* to retain every cell and pass only protein.
  Intended, not demonstrated. Contained use is the classification we are **pursuing**, not one
  we hold. Never write "this is the legal boundary" and never write "in most jurisdictions",
  which is an unsourced claim about law.
- **Modularity.** The expression cassette is a slot, not a rebuild, so the platform outlives
  any one molecule.

The payload we work with, ACC deaminase, has been in the open literature since the 1990s.
Nothing about the biology is proprietary. What is proprietary is everything between the
fermenter and the field.

## Three problems that would stop existing

Not problems we solve. Problems that **would disappear in a working deployment**, because the
protein would not travel. Present tense is not available to us: delivery currently stops at a
reservoir. This is an argument about the architecture, not a description of the 2026 build.

1. **Shelf life.** Peat, the best carrier found, still gives under six months.
2. **The cold chain.** Transit above 40 °C can inactivate a live culture, and Gram-negative
   PGPR do not sporulate, so drying kills them too.
3. **Distance.** Every kilometre is loss, cost and delay the farmer pays for and cannot
   control. Ours is a metre.

**Name the baseline this argument invites, and refuse it.** Our own chassis is Gram-positive
and sporulates, so a dried spore sachet is a real, cheap, ambient-stable competitor to this
entire device, and points 1 and 2 argue for the sachet unless the refusal sits next to them.
The refusal is not shelf life. **It is that a sachet cannot be turned up on Tuesday afternoon
because Thursday looks hot. The reactor answers *how much*. A sachet answers only *whether*.**
That, and retasking: a sachet makes one molecule forever.

## What is true today

Real, measured, ours. Do not inflate and do not add.

- **3 weeks** of unbroken OD600 logging in the chamber, by an instrument we built.
  **Unbroken describes the log, not the culture.** It is not a claim that a culture survived
  three weeks.
- **15 cycles** of design–build–test–learn across reactor, photometer and LED array.
- **3 instruments** built from nothing: perfusion reactor, in-line photometer,
  dual-wavelength LED array.
- **1 failure caught**: our photometer spotted the cross-flow pump dying before we did.

## What is not yet true

State these before a judge finds them. **This list is not exhaustive, and absence from it
proves nothing.**

- **No biological output has been measured.** No induction curve, no titre, no activity
  assay, no plant has received anything. "Brightness is dose" is design intent.
- We have **not measured our own transfer function.**
- **Cells do not grow in the fibre lumen.** No root cause.
- The **second containment layer does not exist.**
- **Delivery stops at a reservoir.** Permeate pump unspecified, root-zone interface deferred.
- **No BOM total**, so every affordability claim is a hypothesis.
- **Membrane cutoff is unchosen.** 0.2 µm and 50 kDa are not two candidate values; they are
  two different devices with opposite consequences, and only one makes "passes only protein"
  true. This is the central unmade design decision, not a note-keeping discrepancy.
- **Contained-use classification unconfirmed** by a Taiwan regulator.
- **Prediction model unvalidated** against a field season.
- **Recurring cost and field infrastructure unaddressed**: feed medium, replacement fibre
  modules, power for the LED array and pumps, network for the forecast, water quality, and who
  stops a weeks-long culture contaminating. The BOM gap is capital cost only; this is the
  other half.

## The people who changed the design

Human practices is a change log, not an attendance record. **An entry without a design change
is a photograph of a meeting and must not appear on a page.** By that rule, six of the nine
entries below are not yet publishable.

- **陳惠雯**, dew-mulch farmer, her farm, **21 July 2026.** Moved dosing off a wall clock onto
  soil-moisture state. *Verbatim sentence not transcribed. Do not invent it.*
- **Dr. Pak K. Yuet**, Dean of Research. 18 Apr 2026: adapt existing reactor designs rather
  than chase novelty. 16 Jul 2026: scale on wall shear and flux below critical, not geometric
  similarity, and declare which similarity group you are sacrificing. *We owe him a written
  justification for hollow-fibre over the packed-bed he recommended.*
- **Dr. Paul Verslues**, **Prof. Cheng**, **Prof. Huang**, **CH Biotech**, **源鮮 YesHealth**,
  the **農民市集** growers, and the public forum: notes not transcribed, no design change on
  record. Cheng and Huang were two separate conversations and must not be merged.

## Context figures (sourced; do not substitute from memory)

These establish that the underserved population is large. **They do not argue that we solve
climate, margins or hunger**, and must never be used to imply it.

- **1.38 billion ha** salt-affected, about **10.7%** of global land. FAO 2024.
- **83%** of drought economic loss lands on agriculture. FAO.
- **84%** of the world's **570 million** farms are under two hectares. FAO.
- Smallholders grow about **one third** of the world's food. Our World in Data. **Never use
  the circulated "70%" figure; it is unsourced and has been corrected.**
- EU biopesticide registration roughly **5–10 years and £3–5 million**; US **$300–400k**.
  Bionema, not re-checked against 2026.

## Facts this brief cannot supply

**If a fact is not in this brief, it is not on record.** You may not assert it, and you may
not assert its negation either. Write "not on record", or ask. Fill these in as they land.

- Does the cassette exist in *B. subtilis* 168, and has 520 nm ever changed any output in our
  hands? **[not on record]**
- 105 minutes to half-maximum **of what**: transcript, intracellular protein, or permeate?
  Which organism, wavelength, citation? **[not on record]**
- **Decay half-life** after the light goes off. **[not on record]**
- **End-to-end field latency**: induction → translation → permeate → reservoir → root zone.
  Necessarily larger than 105 minutes. **[not on record]**
- **Forecast lead time** the controller actually gets. *The prediction argument only closes if
  lead time exceeds end-to-end latency, and we have not checked this.* **[not on record]**
- What the controller **does** with a prediction: threshold, schedule, dose policy.
  **[not on record]**
- ACC deaminase molecular weight and oligomeric state, which is what decides the cutoff.
  **[look it up; do not supply from memory]**
- Reactor dimensions, volume, footprint, power draw, duty cycle, siting. **[not on record]**
- Which strain the three-week OD600 run used, and whether light control was running.
  **[not on record]**
- What kind of second containment layer was asked for. **[not on record]**
- Second wavelength of the dual-wavelength array. Dr. Yuet's institution. **[not on record]**
- Image consent and release for 陳惠雯, CH Biotech and 源鮮. **[not on record]**

## Photographs that exist

Do not specify a photograph that is not on this list; writers invented seven that do not
exist. Seven frames are in `img/`: the team walking into 陳惠雯's field · 陳惠雯 talking in her
plot · hands seating jumper wires beside a printed LED rack and handwritten pin notes · gloved
hands sampling with the membrane cartridge and pump running · a rice grower pointing at his
stall while students take notes · a student writing photometer firmware after school · five
students laughing over a printed part.

**Institutional imagery argues against us.** Cleanrooms, banks of white coats and expensive
instrumentation all say *you need a facility for this*. Ordinary, hand-built and slightly
messy frames argue for us.

## How to write about this

- **Never invent a number, quote, date or result.** No exceptions. This is the project's main
  credibility asset.
- **Do not infer from silence.** A missing fact is not on record. You may not write "we have
  not run a plant trial" any more than "we have".
- No em dashes. Sentence case headings. No AI vocabulary (*delve, leverage, robust, seamless,
  comprehensive, empower, harness, revolutionise*).
- Vary sentence length. Fragments are allowed.
- Prefer showing to claiming. State the limit immediately after the claim it limits, at the
  same type size.

## How not to design it

- **Do not resemble iGEM Brno 2025** (NitroDuck, 2025 Grand Prize). Structurally close thesis,
  so the lane is crowded. Banned: centred farmer facing camera with cupped hands; chat-bubble
  dialogue; round portraits of any kind; confetti between headline words; frosted-glass quote
  cards and `backdrop-filter` anywhere; white pill nav; rounded geometric sans as display;
  word-by-word headline reveals. Worth taking: real named people carry the argument.
- **Do not land in the AI cluster**: cream #F4F1EA + serif + terracotta; near-black with a
  lone acid-green pop; purple-to-blue gradients; Inter or Space Grotesk; emoji as section
  markers; centred text above 600px; italic headings.

## Current build

Homepage: Manifesto structure, Studio theme. Paper `oklch(97.2% .008 95)`, ink
`oklch(21.5% .014 62)`, accent forest green `oklch(44% .098 150)`. Type is the Source
superfamily (Source Serif 4 display 600, Source Sans 3 body, Source Han Serif/Sans TC for
繁體中文, Source Code Pro for data), chosen because Source Han embeds Source Serif and Source
Sans as its own Latin, so Chinese names inside English sentences sit on one baseline. Fully
fluid space scale interpolated 375 → 1400px. **Fonts must be self-hosted and subset**: the
iGEM wiki blocks external font hosts and a full CJK face is 10–20 MB.
