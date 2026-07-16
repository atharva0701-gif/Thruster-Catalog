# Thruster-Catalog

**Bureau Veritas Thruster Requirements — Comprehensive Surveyor Catalog**

A plan-approval reference guide covering the rules, required drawings/documents
and surveyor checklists for marine thruster packages under Bureau Veritas
Rules for Classification of Steel Ships (NR467) and related rule notes.

## Contents

- **`thruster-quickref.html`** — **Interactive quick-reference tool** (recommended
  for day-to-day use). A single self-contained web page: pick the thruster type,
  modifiers (CP / retractable), prime mover, functional roles, ship type and
  notations, and it instantly generates the tailored, tick-off list of drawings
  to demand — grouped by discipline, each tagged FA/FI with its rule reference.
  Works offline, no install; just open it in any browser. Share it by sending the
  single file.
- **`Main.tex`** — LaTeX source of the full detailed guide.
- **`Main.pdf`** — Compiled full guide (~130 pages) — the deep reference behind
  the tool.

## The interactive tool

Open `thruster-quickref.html` in any browser. Features:
- Configuration panel → filtered drawing list for that exact case.
- Live counts (documents / For-Approval / For-Information) and a "received"
  progress bar as you tick items off against a client submission.
- Applicable rule-set chips (NR467 Sec.14/15/7, NR216, IEC 60079, SOLAS, …).
- Identification header, search/filter, print-to-PDF, light/dark theme.
- Ticks auto-save per configuration in your browser.

Ship-type selection auto-adds the relevant special requirements (e.g. tanker →
hazardous-area/Ex; passenger → Safe Return to Port; OSV → DP).

## What the guide covers

- General requirements for all thrusters > 110 kW (drawings, calculations,
  materials, welding, manuals) with **For Approval (FA)** / **For Information
  (FI)** categorisation.
- Per-type drawing/document lists and checklists:
  - Transverse (tunnel & retractable)
  - Rotating / azimuth (fixed- & controllable-pitch) and podded units
  - Water-jet propulsion
  - **Voith-Schneider (cycloidal)** propulsors
  - **Other types** — rim-driven, pump-jet, gill/hydro-jet, steering grid / nozzle
- **Prime-mover considerations** — additional submissions for **electric-motor**
  vs **diesel-engine** driven thrusters (incl. full-train torsional vibration
  calculation for diesel drives).
- Cross-over requirements: **steering gear**, **main shafting**, **hydraulics &
  pitch control**, and **dynamic positioning (DP)**.
- **Ice class & winterisation** (Baltic ice classes, Polar Class, COLD) and
  **additional BV class notations** (COMF, AUT, CLEANSHIP, redundant propulsion,
  service notations).
- Testing & commissioning, common submission errors/red flags, quick-reference
  tables and a consolidated regulatory reference list.

## Building the PDF

```bash
pdflatex Main.tex
pdflatex Main.tex   # run twice for the table of contents and cross-references
```

## Disclaimer

This catalog is a practical reference compiled from BV rules and recognised
standards. Rule references (e.g. NR467 Pt C, Ch 1, Sec 15) and article numbers
must always be verified against the rule edition applicable to the vessel's
contract/build date and class notation. It does not replace the official rules.
