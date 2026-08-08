# House style

For every word published on **Penchal9959**. Written 8 August 2026 from the
inconsistencies found in `AUDIT.md` §E.

The account already reads mostly like one writer. This exists to settle the
handful of places where it does not, and to stop the next pass re-deciding them.

---

## Voice

Plain declarative sentences. Say what the thing is, then what it does, then what
it does not.

Present tense for what the code does. Past tense for what was done to it.

Vary sentence length; average under 25 words. A short sentence after a long one
is how writing breathes.

**No adjective survives without a measurement behind it.** Not "significantly
smaller" — "15.8× smaller than CSV, measured by `compare_formats.py`". If the
number cannot be reproduced from the repository, either cite the command that
produces it or delete the claim.

Limitations go in the same paragraph as the claim they limit, not in a
disclaimer at the bottom. Where something was not verified, the sentence that
mentions it says so.

Team work is labelled as team work, in one paragraph, without naming anyone
else.

## Banned

**Words.** delve, leverage, robust, seamless, cutting-edge, state-of-the-art,
showcase, elevate, harness, unlock, empower, streamline, comprehensive, myriad,
plethora, landscape, realm, testament, underscore, pivotal, crucial, vital,
meticulous, boasts, dive into, embark, navigate (except literally), foster,
holistic, game-changing, revolutionise.

**Not banned when they are the domain term.** `robustness` as a property,
`elevated` of a temperature, `vitals` of a patient, `navigate` of a UI. The ban
is on the marketing sense. Judge by whether a measurement could follow.

**Constructions.**

- "It's not just X — it's Y."
- "In today's fast-paced world…"
- "This project aims to…" or "Welcome to…" as an opening line.
- Three-item lists where two or four is the honest count.
- A Features section that is a bullet list of adjectives.
- Emoji, anywhere. (Arrows `→` `←` in diagrams are not emoji.)
- Bold on more than one phrase per paragraph.
- "Feel free to contribute!", "Happy coding!"
- Rhetorical questions as headings.
- Em dashes above roughly one per paragraph. They are fine; the density is the
  tell.

---

## Vocabulary

One term per concept, everywhere.

| Concept | Use | Never |
|---|---|---|
| Licence, in prose and headings | `Licence` | `License` — **except the file name, which is `LICENSE`**, because GitHub keys its licence detection off that spelling |
| Test bench | `testbench` | "test bench" |
| Place and route | `place and route` (noun), `place-and-route` (attributive) | `P&R`, `PnR` |
| SkyWater process | `SkyWater 130 nm` on first mention per document, `sky130` after | `Sky130`, `SKY130` in prose |
| Levelised scheduling | `levelised` | `levelized` in prose |
| Two-level minimisation | `minimisation` | `minimization` in prose |
| Characterisation | `characterisation` | `characterization` |
| Parameterised, analyse, behaviour, optimise | British | American |

**British spelling in prose. Never in an identifier.** `levelize()`,
`espresso-logic-minimizer`, `zynq-hdmi-rasterizer`, `LICENSE`,
`characterization` inside a file name or a Liberty keyword all stay exactly as
they are. Expect `levelised` in a sentence next to `levelize()` in a code span;
that is correct, not an oversight.

Exact casing: `Verilog` `VHDL` `PyQt5` `AXI4-Stream` `Zynq-7000` `PYNQ-Z2`
`Icarus Verilog` `ModelSim` `ngspice` `Magic` `netgen` `Liberty` `Genus`
`Innovus` `Django` `Arduino` `ESP8266` `Raspberry Pi`.

## Numbers and units

- A space before the unit: `65 nm`, `1.8 V`, `3.060 µm`, `0.005 pF`, `50 ns`.
- `µm`, never `um`. `°C`, never `C` alone for a temperature.
- Digits for 10 and above, and for every measurement. Words below 10 in prose.
- Thousands separated: `180,000 iterations`, `50,074 vectors`.
- Dates as `8 August 2026`.

**Unit spacing is a prose rule only.** A Verilog `` `timescale 1ns/1ps `` is
language syntax. So is `1'b0`, `16'hFFFF`, `#10`. Never touch code.

---

## Structure — active repositories

Same sections, same order, every time.

```
# <Human-readable title>

<One paragraph: what it is, what it targets, what it produces. No preamble.>

## Status
## Repository layout
## Requirements
## Build and run
## Results
## How it works
## Known limitations
## Attribution        <- only where the work was collaborative
## Licence
```

**The specific findings survive as bolded lead-ins, not as headings.** This is
the important rule. "The synthesiser deleted the prefix tree", "REDUCE was doing
nothing", "Hold passes only because a constraint silently failed to apply" are
the most valuable sentences on the account. They move *inside* `## How it works`
or `## Known limitations` and open their paragraph in bold:

> **The synthesiser deleted the prefix tree.** Genus recognised the carry chain
> and replaced it with…

Uniform navigation, specific content. Nothing is flattened into generic prose.

`## Known limitations` is never empty.

Every number in `## Results` is paired with the command that reproduces it.

## Structure — archived repositories

```
# <Name>

**Archived.** <Superseded by [`folder`](link), or: why it is kept.>

## What this was
## Known defects        <- only where a defect exists
## Why it was archived
## Licence
```

**Seven archived repositories carry a defect note and every one must survive**,
rewritten for voice but never softened: `Patient_Monitoring_System` (inverted
clinical thresholds, including "do not use this version as a health monitor"),
`Smart_Vehicle_Detector` (measures distance, not closing speed), `DUAL-PORT-RAM`
(it is single-port), `FSM-SEQUENCE-DETECTOR` (`$display`-only testbench that
cannot fail), `Smart_Dustbin`, `Women_Security_Alarm` and `Smart_Irrigation_…`
(each records what was purged).

---

## Metadata

**Description.** One sentence, **under 120 characters**, no trailing full stop,
same voice as the README's opening line. Archived repositories say so and name
their successor where they have one.

**Topics.** 4–8 per repository, from this list only:

```
hardware design   verilog vhdl rtl digital-design testbench fpga asic vlsi
                  physical-design zynq xilinx
open silicon      sky130 open-source-silicon spice magic standard-cell
design automation eda cad logic-simulation logic-synthesis
                  formal-verification
embedded          arduino esp8266 embedded iot raspberry-pi
software / web    python django pyqt5 gui html css web
state             archived learning
```

The list was extended once, on 8 August 2026: the original was drawn from the
hardware repositories and had no honest tag for the PyQt5 interface or the
HTML and CSS exercises, which would have forced either a wrong tag or fewer
than four. Extend it again the same way if that happens — deliberately, in this
file — rather than inventing a tag at the point of use.

**Descriptions are set in one place only.** Phase 3 of `apply.ps1` used to
overwrite corrected descriptions on every run and was deleted for it. Do not
reintroduce a second writer.

**Badges** belong on the profile README and nowhere else. A profile page is a
front door; a project page is documentation.

## Licensing

MIT everywhere, including archived. A public repository with no licence is "all
rights reserved" by default, which is not the intent for a record of learning
work.

Two repositories need a note that MIT does not cover everything in them:

- **`FamilyTree-Django`** — the vendored Bootstrap, jQuery, Font Awesome and
  Montserrat under `vendor/` and `fonts/` keep their own licences.
- **`HTML-CSS`** — the seven sample photographs were collected from the web
  while learning and their provenance was never recorded.

## Never

No project report, poster, certificate page, title slide, roll number, course
code, institute name, or another person's name, e-mail or phone number — in any
repository, at `HEAD` or in history, in any file type.

**Two exceptions, and they are not loopholes.**

**Upstream licence attribution always wins.** BSD, MIT and Apache all *require*
retaining the copyright holder's name. `zynq-hdmi-rasterizer` credits **Florent
Werbrouck** for the PYNQ-Z2 video-out example its `sw/` derives from, under BSD
3-Clause, and that name must stay. This was nearly removed once by reading the
rule above too literally. The rule is about a co-author's personal data attached
to academic work without their say; a licence notice is the opposite — a name
the licence obliges you to publish.

`IIT Bombay` on the **profile** README is the one exception, and it is
deliberate: a current affiliation on a personal profile is not a college name
embedded in a project artefact.
