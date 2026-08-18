# ReLeaf — iGEM 2026 wiki homepage

**GEMS Taiwan · Biomanufacturing Village**

> Micro-Factories for Micro-Farmers: Democratizing Bio-Production.

A perfusion hollow-fibre membrane bioreactor that produces plant bioprotectants
on site, on demand, at the moment the crop needs them. This repository holds the
homepage prototype for the competition wiki.

## Files

| File | What it is |
|---|---|
| `index.html` | Current homepage, v0.4. Single file, no build step, no external requests. |
| `index_v3_backup.html` | v0.3, kept for reference. Organised around one claim (proportional light). |
| `index_v1_dataforward.html`, `index_v2_brno-marburg.html` | Earlier direction studies. |
| `PHOTO_SHOTLIST.md` | Every photo slot on the page, with a shooting brief. Slots are `data-shot="P-nn"`. |
| `ASSETS_NEEDED.md` | Non-photo assets still outstanding. |
| `HOMEPAGE_BENCHMARK.md` | Study of 8 agri-biotech homepages (Bayer, Syngenta, Corteva, BASF, Pivot Bio, Indigo, Ginkgo, Hello Tractor) and what to take from each. |

## Running it

No build step. Open `index.html`, or serve the folder:

```bash
python3 -m http.server 8811
```

## Reading the page

- **Dashed boxes** are photo slots. Replace with `<img>`, keeping the wrapper classes.
- **Amber** marks anything not yet earned: an unverified number, a missing quote, an
  open engineering problem. Nothing amber should survive to wiki freeze without either
  evidence behind it or removal.
- The hero slider is the one thing on the page a visitor can operate. Drag it and the
  light follows instantly while the protein number crawls, which is the project's
  central constraint felt rather than read.

## Structure

Hero → problem (farmer's side) → problem (bioprotectant logistics) → solution and its
three elements → synbio → what we built and measured → integrated human practices →
product highlights → future goal and stated limits → team.

## Before freeze

The page carries its own to-do list in amber. The largest items: the real sensor log to
replace the modelled hero trace, five outstanding interview quotes, cost per unit from a
real BOM, membrane cutoff, and confirmation of contained-use classification from a
Taiwan regulator rather than from us.
