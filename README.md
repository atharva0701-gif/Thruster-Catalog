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

Open `thruster-quickref.html` in any browser — **this is the local app**. No
internet, no install, no account, no Claude access needed: just double-click
the file (or open it from an email attachment) and it runs entirely offline
on your work computer, a locked-down machine, or a phone.

Configuration inputs → a filtered, tailored drawing list:
- Thruster type, **controllable-pitch / retractable / contra-rotating (CRP —
  azimuth \& podded units)**.
- **Duty: manoeuvring / propulsion / take-me-home** (propulsion duty correctly
  pulls in the main-shaft-line package and a mandatory torsional vibration
  calculation; manoeuvring does not).
- **Propeller: open / ducted (nozzle)**, with fixed vs. **steering nozzle**
  (steering nozzle correctly pulls in the steering-gear package).
- Prime mover, functional role, ship type, and Part-F additional notations.

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

> **Rule references verified (Jan 2026):** notations and ship-type/service
> designations are formally listed in **NR467 Part A, Ch.1** (Principles of
> Classification and Class Notations); the technical requirements for each then
> sit in **Part D** (general service notations), **Part E** (OSV & tugs), and
> **Part F** (additional class notations — ice, COMF, AUT, CLEANSHIP,
> MON-SHAFT, **DYNAPOS** for DP). DP is additional class notation DYNAPOS in
> Part F — not "NR216", which is actually the Materials & Welding rule note.

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
