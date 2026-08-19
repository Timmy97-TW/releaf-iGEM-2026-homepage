# Type — the decision, and what has to happen before freeze

## What we use, and why

| Role | Face | Why this one |
|---|---|---|
| Display | **Source Serif 4**, SemiBold 600 | Sturdy old-style serif. Agricultural bulletin register, not fashion magazine. Has real display weight, so it holds against a photograph. |
| Body | **Source Sans 3**, 400 / 700 | Humanist, warm, wide language coverage, reads well at 17–19 px. |
| 繁體中文 | **Source Han Serif TC** (思源宋體) · **Source Han Sans TC** (思源黑體) | See below. This is the whole reason for the choice. |
| Data | **Source Code Pro**, 400 | Tabular figures for dates and measurements. |

All four are SIL Open Font License. Free to use, free to self-host, free to modify.

## The reason it is the Source family and not something prettier

Source Han Serif **embeds Source Serif as its own Latin**, and Source Han Sans embeds
Source Sans. So when the page sets

> 陳惠雯 walked us through her field

the Chinese and the English come from faces that were drawn to sit together, on one
baseline, at one optical weight. Nearly every other pairing produces a visible seam in the
middle of that sentence, and this page puts Chinese names inside English sentences
constantly. It is the one typographic problem unique to this wiki, and this is the pairing
that solves it.

**What we replaced and why.** v0.6 shipped with Didot / Bodoni 72. Three problems: it is a
Didone, which reads as luxury fashion and fights a page about handing tools to smallholders;
it ships on macOS only, so Windows and Linux judges silently got Georgia and a different
design; and it has no Chinese at all.

## Before wiki freeze: self-host

**The iGEM wiki blocks external font hosts.** A `fonts.googleapis.com` link will silently
fail and the page will fall back to Georgia. Everything below must be self-hosted on
`static.igem.wiki`.

### 1. Get the files

```bash
pip install fonttools brotli
```

Source Serif 4 and Source Sans 3: download from Google Fonts or the Adobe GitHub releases.
Source Han Serif TC / Source Han Sans TC: use the **Noto** builds, which are the same fonts
(Noto Serif TC, Noto Sans TC).

### 2. Subset, or the page will be unusable

A full CJK font is **10–20 MB**. Do not ship one. This page currently uses twelve unique
Chinese glyphs, so a subset is a few kilobytes.

```bash
pyftsubset NotoSerifTC-SemiBold.otf \
  --text="思源宋體黑農民市集陳惠雯產銷班輪灌稻作訪談" \
  --flavor=woff2 --output-file=NotoSerifTC-subset.woff2
```

Re-run that with the full set of Chinese actually on the page every time the copy changes.
Missing a glyph is worse than a slightly larger file, so err on the side of including more.

Latin faces subset to Latin-1 plus the punctuation we use:

```bash
pyftsubset SourceSerif4-SemiBold.otf \
  --unicodes="U+0000-00FF,U+2018-201D,U+2022,U+2026,U+00B7,U+2192,U+00D7,U+207B,U+00B0" \
  --flavor=woff2 --output-file=SourceSerif4-SemiBold-subset.woff2
```

### 3. Declare them

```css
@font-face{
  font-family:"Source Serif 4"; src:url("SourceSerif4-SemiBold-subset.woff2") format("woff2");
  font-weight:600; font-style:normal; font-display:swap;
  unicode-range:U+0000-00FF,U+2018-201D,U+2022,U+2026,U+00B7,U+2192;
}
@font-face{
  font-family:"Source Han Serif TC"; src:url("NotoSerifTC-subset.woff2") format("woff2");
  font-weight:600; font-style:normal; font-display:swap;
  unicode-range:U+4E00-9FFF,U+3000-303F,U+FF00-FFEF;
}
```

The `unicode-range` split matters: it stops the browser downloading the Chinese file for a
visitor who only ever sees English, and vice versa.

Weights actually needed: **Source Serif 4 600**, **Source Sans 3 400 and 700**,
**Source Code Pro 400**, plus the two CJK faces at one weight each. Six files. Do not ship
a weight the page does not use.

`font-display:swap` is deliberate. The fallback chain below is chosen to be survivable, so a
visitor on a slow connection reads the page immediately in Georgia rather than staring at
nothing.

## The scale

Set once as tokens in `tokens.css`, referenced by name everywhere.

| Token | Size | Leading | Tracking | Used for |
|---|---|---|---|---|
| `--text-display` | 44 → **92 px** | 0.98 | −0.025em | Hero headline only |
| `--text-display-s` | 31 → 52 px | 1.06 | −0.018em | Section claims |
| `--text-4xl` | 24 → 34 px | 1.15 | −0.012em | Sub-heads, stat numbers |
| `--text-lede` | 19 → 23 px | 1.5 | — | Hero deck, section ledes |
| `--text-base` | 17 → 19 px | 1.65 | — | Body |
| `--text-sm` | 15 px | 1.6 | — | Captions |
| `--text-xs` | 12 px | — | .18em, caps | Labels |

**Why 92 px and not larger.** "biomanufacturer" is fifteen characters. Past roughly 92 px it
stops reading as a headline and starts reading as a wall, and the photograph underneath it
stops being visible. The previous build capped at 102 px and the hero was worse for it.

**Tracking runs in opposite directions by script.** Latin display is tightened (−0.025em)
because large type opens up naturally. Chinese is *loosened* (+0.02em) and given far more
leading (1.78 against 1.65), because CJK glyphs are dense squares and tight leading closes
the page in. This is handled by `:lang(zh)`, so mark Chinese runs with `lang="zh-Hant"`.

**Measure.** Body caps at 62ch, ledes at 46ch. For a full Chinese paragraph aim for 35–40
characters per line instead, since CJK glyphs are roughly double width.
