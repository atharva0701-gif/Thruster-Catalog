# Thruster-Catalog

**Bureau Veritas Thruster Requirements — Comprehensive Surveyor Catalog**

A plan-approval reference guide covering the rules, required drawings/documents
and surveyor checklists for marine thruster packages under Bureau Veritas
Rules for Classification of Steel Ships (NR467) and related rule notes.

## Contents

- **`thruster-quickref.html`** — **Interactive quick-reference tool** (recommended
  for day-to-day use). A single self-contained web page: pick the thruster type,
  rated power, duty, propeller configuration, prime mover, steering arrangement,
  ship type, ice class and notations, and it generates the tailored, tick-off list
  of documents to demand. **Every line is traceable to a named rule table row or
  article** (e.g. *NR467 Pt C, Ch 1, Sec 15, Tab 1 #2*) and carries the rule's own
  **A / I** categorisation. Works offline, no install; share by sending the single file.
- **`BV-Rules-Verification.md`** — the verification database: what was checked on
  BV Rules Explorer, what the live rule says, and where the catalog diverged.
  Read this before trusting any citation in the PDF.
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

Open `thruster-quickref.html` in any browser — **this is the local app**. No
internet, no install, no account, no Claude access needed: just double-click
the file (or open it from an email attachment) and it runs entirely offline
on your work computer, a locked-down machine, or a phone.

**Rule basis:** transcribed from BV Rules Explorer — **NR467 edition Jul 2026**
(Pt C, Ch 1, Sec 15 Tables 1–5; Sec 14 Table 1 #13 and Article 4; Pt C, Ch 2,
Sec 4; Pt F, Ch 8 and Ch 11 Sec 5) and **NR584 edition Apr 2026**.

Configuration inputs → a filtered, tailored submission list:
- Thruster type (transverse, retractable, azimuth Z/L, podded, water-jet,
  Voith-Schneider, rim-driven, pump-jet, gill-jet) with CP / retractable / CRP.
- **Rated power ≥ or < 110 kW** — below the threshold the Sec 15 tables do not
  apply at all ([1.1.2]), and the tool says so instead of listing drawings.
- **Duty: manoeuvring / propulsion / propulsion + steering.** This drives the
  real rule consequences: manoeuvring-only omits the 10% propeller thickness
  increase, sizes the shaft by the Sec 15 formula rather than Sec 7, uses
  auxiliary rather than propulsion gear safety factors, and does not require
  Surveyor-witnessed material tests.
- **Propeller: open / ducted**, with a warning when a *fixed* nozzle propulsion
  propeller is selected — those are **not thrusters** per Sec 15 [1.2.1] and
  belong under Sec 8.
- Prime mover (electric drive > 1 MW adds the Ch 2, Sec 4 [5.1.1] assembly tests),
  steering arrangement (single vs multiple units), DP with **R/RS gating on the
  FMEA**, ice class (manoeuvring transverse thrusters get **tunnel grids only**),
  and 24 ship types each mapped to its governing publication.

Alongside the document list the tool emits a **Rule verification checks** panel —
the numeric criteria a surveyor must confirm: 2,3°/s main and 0,5°/s auxiliary
steering rates, the 45 s / 30 min / 10 min alternative power supply, the
2 500 kW-per-unit thresholds, tunnel thickness ≥ adjacent hull, the two-azimuth-
thruster rule for sole-means-of-propulsion, and the minimum Tab 6 alarms.

Other features:
- Live counts (documents / For-Approval / For-Information) and a "received"
  progress bar as you tick items off against a client submission — ticks
  auto-save per configuration in your browser.
- Applicable rule-set chips (NR467 Pt A/C/D/E/F, NR216/NR266/NR320/NR500/NR527/
  NR566, IEC 60079, SOLAS, …).
- Identification + specification header (maker/model, power/thrust/rpm/supply).
- Search/filter, print-to-PDF, light/dark theme.

**Getting the list into Excel (mobile-safe, three ways, most reliable first):**
1. **Copy for Excel / Sheets** — copies a tab-separated table to the clipboard.
   Open Excel/Sheets/Numbers, tap a cell, paste — it fills in as columns
   instantly. This is the recommended path on mobile, where browser
   file-download can be unreliable (silently blocked in email in-app
   browsers/older WebViews with no error shown).
2. **Download .csv file** — triggers a normal file download for
   desktop browsers; on mobile it also reveals a visible, pre-selected
   fallback text box so you can manually copy the data even if the automatic
   download didn't fire.
3. **Copy as checklist text** — a plain-text tick-list for pasting into an
   email or notes app.

Ship-type selection auto-adds the relevant special requirements (e.g. tanker →
hazardous-area/Ex; passenger → Safe Return to Port; OSV → DP).

> **Rule references verified against NR467 Jul 2026 on BV Rules Explorer.**
> Notations and ship-type/service designations are formally listed in **NR467
> Part A, Ch.1**; the technical requirements sit in **Part D** (general service
> notations), **Part E** (OSV & tugs), and **Part F** (additional class notations
> — ice, COMF, AUT, CLEANSHIP, MON-SHAFT, **DYNAPOS** for DP). DP is additional
> class notation DYNAPOS in Part F — not "NR216", which is the Materials &
> Welding rule note. Full evidence trail in `BV-Rules-Verification.md`.

> ✅ **The tool and the PDF are in sync (v1.8).** Both are anchored to the same
> transcribed rule tables. The PDF's **Chapter 1 — "The Rule-Mandated
> Submissions (Authoritative)"** reproduces NR467 Sec 15 Tables 1–5, Sec 14
> Tab 1 #13 and Article 4, Pt C Ch 2 Sec 4 [5.1.1], the DYNAPOS table, the
> Pt F Ch 8 ice split and all four NR584 tables, verbatim with the rule's own
> **A/I** categories. Later chapters are explicitly marked as *supporting
> surveyor practice*, not rule-mandated deliverables.

## What the guide covers

- General requirements for all thrusters ≥ 110 kW (drawings, calculations,
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
