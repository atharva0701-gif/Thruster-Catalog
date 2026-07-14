# Thruster-Catalog

**Bureau Veritas Thruster Requirements — Comprehensive Surveyor Catalog**

A plan-approval reference guide covering the rules, required drawings/documents
and surveyor checklists for marine thruster packages under Bureau Veritas
Rules for Classification of Steel Ships (NR467) and related rule notes.

## Contents

- **`Main.tex`** — LaTeX source of the guide.
- **`Main.pdf`** — Compiled guide (~100 pages).

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
