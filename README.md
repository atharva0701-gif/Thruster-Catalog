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
- **`Thruster-Package-Register.xlsx`** — **Admin intake & package-tracking
  workbook** (see below).
- **`build_thruster_register.py`** — generator script for the workbook.

## Admin intake & package tracking (`Thruster-Package-Register.xlsx`)

Solves the problem of thruster drawings arriving in tranches over ~6 months
(mechanical → hydraulic → electrical/control → TVC) where non-technical admins
otherwise open several review packages for one thruster. A shared workbook keyed
on the **client PO number** so no technical judgement is needed:

- **Read me first (SOP)** — the golden rule, step-by-step intake procedure, and a
  client acknowledgement-email template.
- **Package Register** — one row per thruster package (BV Reg No, PO, client,
  vessel, thruster tag/type, per-discipline received-dates, auto "still
  outstanding" column, status). Duplicate PO numbers are flagged automatically.
- **Intake Log** — one row per incoming submission; type the PO number and the
  **ACTION** column auto-tells the admin *"✓ EXISTING — route to BV-Reg-XXX"* or
  *"➤ NEW PACKAGE — create BV registration"* (green/amber highlighted).

Put the file on the shared drive / SharePoint so all admins update the same copy.

## The interactive tool

Open `thruster-quickref.html` in any browser — **it runs fully offline**, no
internet or install needed (it *is* the local app; double-click the file). Features:
- Configuration panel → filtered drawing list for that exact case. Inputs:
  thruster type, **controllable-pitch / retractable**, **duty (manoeuvring /
  propulsion / take-me-home)**, **propeller: open / ducted (fixed or steering
  nozzle)**, prime mover, functional role, ship type and Part-F notations.
- Live counts (documents / For-Approval / For-Information) and a "received"
  progress bar as you tick items off against a client submission.
- Applicable rule-set chips (NR467 Pt C/D/E/F, NR216/NR266/NR527/NR500/NR566,
  IEC 60079, SOLAS, …).
- **Export to Excel/CSV** and **copy list**; identification + specification
  header (power/thrust/rpm/supply); search/filter; print-to-PDF; light/dark.
- Ticks auto-save per configuration in your browser.

Ship-type selection auto-adds the relevant special requirements (e.g. tanker →
hazardous-area/Ex; passenger → Safe Return to Port; OSV → DP).

> **Rule references verified (Jan 2026):** DP = additional class notation
> **DYNAPOS** in **NR467 Part F** (not "NR216" — NR216 is Materials & Welding).
> Service notations: Part D (general), **Part E (OSV & tugs)**; additional class
> notations (ice, COMF, AUT, CLEANSHIP, MON-SHAFT, DYNAPOS): **Part F**.

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
