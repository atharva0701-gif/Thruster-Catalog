# BV Rules Explorer Verification Log

> **Round 2 (2026-07-16, deep pass)** — the sections below marked **§7 onwards** record a
> full transcription of the actual NR467 Sec 15 / Sec 14 / Pt F submission tables and the
> discovery of **NR584**, a dedicated azimuth-thruster rule note that the catalog had never
> cited. `thruster-quickref.html` was rebuilt against these transcribed tables.

Verification of the publications, rule references, and ship-type coverage cited in
`Main.tex` (Thruster Requirements Catalog v1.6) against the live **Bureau Veritas
Rules Explorer** (https://rulesexplorer.bureauveritas.com/), checked on 2026-07-16.

This file is a running database: each entry records what was checked, what the
live source says, and whether the catalog matches. Re-run these checks whenever
NR467 issues a new edition (check the edition dropdown on Rules Explorer) or before
relying on this catalog for a live plan-approval decision.

Source edition checked: **NR467, Jul 2026 (Latest Edition)**, cross-checked against
**Jan 2026** where noted. Catalog's own "Verified against NR467 Jan 2026" claim
(v1.5/v1.6 changelog) is now one edition behind; Jul 2026 supersedes it.

---

## 1. Related BV Rule Notes — existence & title check

All eight rule notes cited in Main.tex §"Related BV Rule Notes" were searched
individually on Rules Explorer's Publications list. **All eight exist and titles match.**

| Publication ID | Catalog's title | Rules Explorer title (live) | Latest edition | Status |
|---|---|---|---|---|
| NR216 | Materials and Welding | Rules on materials and welding for the classification of marine units | Jan 2025 | ✅ Match |
| NR266 | Requirements for Survey of Materials and Equipment | Requirements for survey of materials and equipment for the classification of ships and offshore units | Mar 2026 | ✅ Match |
| NR320 | Certification scheme of materials and equipment for marine units | Certification scheme of materials and equipment for the classification of marine units | May 2025 | ✅ Match |
| NR527 | Ships operating in polar waters / icebreakers | Ships operating in polar waters and icebreakers | Jan 2026 | ✅ Match |
| NR500 | Classification and certification of yachts | Rules for the classification and the certification of yachts | Oct 2024 | ✅ Match |
| NR566 | Hull arrangement, stability and systems for ships < 500 GT | Hull arrangement, stability and systems for ships less than 500 GT | Nov 2024 | ✅ Match |
| NR483 | Classification of naval ships | Rules for the classification of naval ships | Dec 2025 | ✅ Match |
| NR445 | Classification of offshore units (MODU/drillships) | Rules for the classification of offshore units | Jun 2025 | ✅ Match |

**Finding:** No fabricated or mistitled rule notes. All eight are real, current BV publications.

**Not cited by catalog but exists / worth knowing about:**
- **NR610** — Rules for the Classification of Diving Systems. Referenced inside NR467 Part A Ch.1 §1.1.3 as taking precedence over NR467 for diving systems. Relevant if a Diving Support Vessel (Part E Ch.7 — see §3 below) thruster package intersects with the diving system itself. Not currently in the catalog's reference list.
- **NR645** — Floating storage regasification units / floating storage units. Not thruster-catalog-relevant unless scope expands to FSRU/FSU.
- **NR217** — Inland navigation vessels. Out of scope (catalog is for sea-going ships per its own Part A citation).

---

## 2. NR467 Part / Chapter / Section structure

Live ToC (Jul 2026) confirms the catalog's structural claims almost exactly.

| Catalog claim | Live Rules Explorer (Jul 2026) | Status |
|---|---|---|
| Part A Ch.1 = master index of ship types/notations | Part A, Chapter 1: "Principles of Classification and Class Notations", Section 2: "Classification Notations" | ✅ Match |
| Part B = Hull and Stability | Part B: Hull and Stability | ✅ Match |
| Part C = Machinery, Electricity, Automation and Fire Protection | Part C: Machinery, Electricity, Automation and Fire Protection | ✅ Match |
| Part C Ch.1 Sec.2 = Diesel Engines | Section 2: Diesel Engines | ✅ Match |
| Part C Ch.1 Sec.7-8 = Shaft Lines and Propellers | Section 7: **Main Propulsion Shafting**, Section 8: **Propellers** | ✅ Match (catalog's shorthand "Shaft Lines" ≈ actual "Main Propulsion Shafting") |
| Part C Ch.1 Sec.14 = Steering Gear | Section 14: Steering Gear | ✅ Match |
| Part C Ch.1 Sec.15 = Thrusters (and water-jets) | Section 15: **Thrusters** | ✅ Match — but see discrepancy below re: water-jets |
| Part D = Service Notations | Part D: Service Notations | ✅ Match |
| Part E = Service Notations for Offshore Service Vessels and Tugs | Part E: Service Notations for Offshore Service Vessels and Tugs | ✅ Match |
| Part F = Additional Class Notations | Part F: Additional Class Notations | ✅ Match |
| DYNAPOS lives in Part F | Confirmed: **Part F, Chapter 11, Section 5** ("Manoeuvring, Mooring, Anchoring and Position Keeping") | ✅ Match, and catalog's v1.5 self-correction (moving DP off "NR216") is verified correct |

### Discrepancies found

1. **Power threshold wording (Ch.1 / §Applicability of catalog).** Catalog says thrusters "**exceeding** 110 kW" (i.e. > 110 kW) attract the full Sec.15 package. Live rule text (Part C, Ch.1, Sec.15, Art.1.1.1) says thrusters developing power **"equal to 110 kW or more"** — i.e. **≥ 110 kW**, and Art.1.1.2 explicitly carves out "less than 110 kW" as the reduced-package case. **A thruster rated at exactly 110 kW is in-scope for the full package under the real rule, but the catalog's "exceeding 110kW" wording would incorrectly exclude it.** Confirmed identical wording in both Jan 2026 and Jul 2026 editions, so this isn't an edition-drift issue — it's a wording error in the catalog that should be fixed to "≥110 kW" / "110 kW or more."

2. **DYNAPOS notation suffixes (Document Purpose chapter, Part F bullet list).** Catalog lists the DP notation family as "DYNAPOS (AM / AT / ATR, SAM / SAT)". Live rule text (Part A Ch.1 Sec.2 [6.21.5] and Part F Ch.11 Sec.5) gives the actual notations as **AM, AT, AM/AT, SAM**, with redundancy-qualified variants **AM/AT R** and **AM/AT RS**. "ATR" and "SAT" as written in the catalog do not match any notation string found on Rules Explorer — they appear to be typos/compressions of "AM/AT R" and possibly a non-existent "SAT". Recommend correcting to: DYNAPOS (AM / AT / AM-AT / AM-AT R / AM-AT RS / SAM).

3. **Redundant-propulsion notation name (Regulatory References chapter, Part F bullet list).** Catalog lists "Redundant propulsion — RP / AVM notations". Live search for "redundant propulsion" surfaces **AVM-DPS** (Part F, Ch.2, Sec.2) as the actual notation for ships with redundant propulsion/steering, plus the related **HEADING CONTROL / HEADING CONTROL-DS / HEADING CONTROL-IS** notations (Part F Ch.11 Sec.2) which are about maintaining heading with redundant propulsion in adverse weather — thematically close to escort-tug/DP use cases in the catalog but not mentioned anywhere in Main.tex. No notation called bare "RP" was found. Recommend changing "RP / AVM" to "AVM-DPS", and considering a short cross-reference to HEADING CONTROL-DS/IS in the tug/escort-tug and offshore-vessel sections.

4. **MON-SHAFT — confirmed correct.** Part F, Ch.5, Sec.2 defines MON-SHAFT ("Tailshaft monitoring system"), explicitly for "oil or water lubricated systems for tailshaft bearings **and podded propulsions**." Matches catalog's dedicated MON-SHAFT section and its cross-reference from the Podded Propulsion chapter. No issue.

5. **Water-jets under Section 15.** Catalog's header note says Section 15 covers "Thrusters (and water-jets)". The live Section 15 Article 1.1.1 text found in this check only explicitly names "transverse thrusters intended for manoeuvring" and azimuth thrusters; water-jets were not seen explicitly in the excerpt pulled. This isn't a confirmed error — Section 15 is long and water-jets may be addressed in an article not surfaced by the search terms used — but it wasn't independently confirmed either. **Flag for follow-up**, not a hard discrepancy.

---

## 3. Ship-type / service-notation coverage (Part D + Part E)

Full live chapter lists pulled from Rules Explorer's ToC tree.

### Part D : Service Notations — 17 chapters (general seagoing ship types)
1. Ro-Ro Cargo ships and Pure Car and/or Truck Carriers
2. Container Ships
3. Livestock Carriers
4. Bulk Carriers
5. Ore Carriers
6. Combination Carriers
7. Oil Tankers and FLS Tankers
8. Chemical Tankers
9. Liquefied Gas Carriers
10. Tankers
11. Passenger ships
12. Ro-Ro Passenger ships
13. Ships for Dredging Activity
14. Non-Propelled Units
15. Fishing Vessels
16. Offshore Patrol Vessels
17. Cement Carriers

### Part E : Service Notations for Offshore Service Vessels and Tugs — 12 chapters
1. Tugs (tug / salvage tug / escort tug)
2. Anchor Handling Vessels
3. Supply Vessels
4. Fire Fighting Ships
5. Oil Recovery Ships
6. Cable-Laying Ships
7. Diving Support Vessels
8. Lifting Units
9. Semi-Submersible Cargo Ships
10. Standby Rescue Vessels
11. Accommodation Units
12. Pipe Laying Units

### Coverage cross-check against the catalog's Ship-Type → Thruster Expectation Matrix (Ch.14)

| Catalog row | Real BV chapter(s) it maps to | Status |
|---|---|---|
| Harbour / escort tug | Part E Ch.1 Tugs | ✅ Covered |
| Offshore supply / PSV / AHTS | Part E Ch.2 Anchor Handling Vessels + Ch.3 Supply Vessels | ✅ Covered (catalog merges two real chapters into one row — reasonable) |
| Dredger (TSHD/CSD) | Part D Ch.13 Ships for Dredging Activity | ✅ Covered |
| Passenger ship / RoPax / ferry | Part D Ch.11 Passenger ships, Ch.12 Ro-Ro Passenger ships | ✅ Covered |
| Cruise ship | Subset of Part D Ch.11 | ✅ Covered (no separate BV chapter for "cruise ship" — correct that it's folded into Passenger ships) |
| Double-ended ferry | Subset of Part D Ch.12 | ✅ Covered (no distinct BV chapter — correctly treated as an operational variant, not a notation) |
| Cable/pipe layer, offshore construction | Part E Ch.6 Cable-Laying Ships + Ch.12 Pipe Laying Units | ✅ Covered |
| Drillship/semi-sub (MODU) | Not in NR467 at all — governed by **NR445** (separate rule) | ✅ Correctly routed to NR445, not NR467 |
| Oil/chemical tanker | Part D Ch.7 Oil Tankers and FLS Tankers, Ch.8 Chemical Tankers, Ch.10 Tankers | ✅ Covered |
| Gas carrier (LNG/LPG) | Part D Ch.9 Liquefied Gas Carriers | ✅ Covered |
| Ice-class / polar trader | Part F additional notation (ice class), not a Part D/E chapter | ✅ Correctly treated as an additional notation, not a service notation |
| Research / naval / patrol | Part D Ch.16 Offshore Patrol Vessels (partial — "patrol" only); naval ships routed to NR483 | ⚠️ Partial — "Research" vessel has no obvious Part D/E chapter or dedicated rule note found in this check; may not need one, but wasn't confirmed |
| Large yacht | Routed to NR500 (separate rule) | ✅ Correctly routed |
| Container/bulk/general cargo | Part D Ch.2 Container Ships, Ch.4 Bulk Carriers | ✅ Covered; "general cargo" has no dedicated chapter, consistent with catalog's own note "no special service overlay" |

### Gaps — real BV service notations with NO row in the catalog's matrix

These are valid, current NR467 Part D/E chapters that a thruster surveyor could plausibly encounter, but which the catalog's ship-type chapter (Ch.14) does not mention at all:

- **Part E Ch.4 — Fire Fighting Ships.** Only referenced obliquely as "FiFi where fitted" under the PSV row; no dedicated treatment despite fire-fighting ships/tugs having distinct pump-drive/power-takeoff interactions with thrusters.
- **Part E Ch.5 — Oil Recovery Ships.** Not mentioned anywhere in Main.tex.
- **Part E Ch.7 — Diving Support Vessels.** Not mentioned anywhere. **This is the most notable gap** — DSVs are almost always DP-2/DP-3 with multiple azimuth/tunnel thrusters, arguably as thruster-intensive as the PSV/OSV or cable-lay rows the catalog already covers in detail.
- **Part E Ch.8 — Lifting Units.** Not mentioned (heavy-lift/crane vessels are frequently DP-equipped).
- **Part E Ch.10 — Standby Rescue Vessels.** Not mentioned.
- **Part E Ch.11 — Accommodation Units.** Not mentioned (likely low thruster-relevance if non-propelled, but not confirmed either way).
- **Part D Ch.3 — Livestock Carriers**, **Ch.6 — Combination Carriers**, **Ch.14 — Non-Propelled Units**, **Ch.15 — Fishing Vessels**, **Ch.17 — Cement Carriers.** None mentioned; likely low-priority (standard bow-thruster-only cases similar to the catalog's cargo/bulk row) but not explicitly confirmed as such.

**Recommendation:** at minimum, add a Diving Support Vessel row to the Ch.14 matrix (Part E Ch.7) given how thruster/DP-heavy that vessel class is — it's a materially bigger gap than the others.

---

## 4. Part F additional-notation chapter list — cross-check

Live Part F has 16 chapters. Catalog's Part F bullet list (Regulatory References chapter) maps as follows:

| Catalog bullet | Real Part F chapter | Status |
|---|---|---|
| Ice class / Polar Class / COLD winterisation | Ch.8 Navigation in Cold Environment | ✅ Covered |
| Comfort on board (COMF-NOISE, COMF-VIB) | Ch.6 Comfort on Board and Habitability | ✅ Covered |
| Automated machinery spaces (AUT-UMS/CCS/PORT) | Ch.3 Automation Systems (AUT) | ✅ Covered |
| DYNAPOS | Ch.11 Manoeuvring, Mooring, Anchoring and Position Keeping | ✅ Covered (see notation-suffix discrepancy in §2) |
| CLEANSHIP / EAL | Ch.9 Environmental Protection | ✅ Covered |
| Redundant propulsion (RP/AVM) | Ch.2 Availability of Machinery (AVM) | ⚠️ See naming discrepancy in §2 (real notation is AVM-DPS, not "RP") |
| MON-SHAFT | Ch.5 Monitoring Equipment | ✅ Covered, confirmed correct |

**Part F chapters that exist but are never cited in the catalog, despite thruster relevance:**
- **Ch.14 — Electric Propulsion or Power Supply.** Not cited anywhere, despite the catalog having an entire chapter (Ch.7, "Prime Mover Considerations") on electric-motor-driven thrusters. Worth checking whether this Part F chapter defines a notation (e.g. for full electric propulsion plants) that would apply to podded/azimuth electric thruster installations.
- **Ch.15 — Elastic Shaft Alignment and Hydroelasticity.** Not cited anywhere, despite the catalog's Ch.9 ("Thrusters as Part of Main Shafting") covering alignment in detail.
- **Ch.4 — Integrated and digital Systems.** Not cited; the catalog does reference IACS UR E22/E26/E27 (cyber-resilient control systems) in its external-standards list, which is thematically the same territory, so this may just be a naming/cross-reference gap rather than a missing topic.

---

## 5. Items in the catalog NOT verifiable against Rules Explorer

Rules Explorer only hosts Bureau Veritas publications (NR/NI numbers). The following catalog citations are external standards bodies and were **not** checked in this pass — they'd need to be verified against ISO, IEC, IACS, or IMO's own portals instead:

- ISO 6336, ISO 22547, ISO 484, ISO 4413, ISO 20283 / ISO 6954
- IEC 60092 series, IEC 60034, IEC 61508, IEC 60079
- IACS UR I1-I3, UR M, UR E22/E26/E27
- SOLAS II-1/29, II-1/8-1, II-2/21-22, II-2, V/28
- IGC Code, IMO MODU Code, HSC Code
- IMO Res. A.468(XII), MSC.337(91), MSC/Circ.645, MSC.1/Circ.1580, MSC.1/Circ.1369
- Finnish-Swedish Ice Class Rules (TRAFICOM)

---

## Summary

| Category | Checked | Confirmed correct | Discrepancies / gaps found |
|---|---|---|---|
| Related BV Rule Notes (NR216/266/320/527/500/566/483/445) | 8 | 8 | 0 |
| NR467 Part A-F top-level structure | 6 | 6 | 0 |
| NR467 Part C thruster/steering/shafting sections | 4 | 4 | 0 (structure), 1 (wording: ≥110kW vs >110kW) |
| DYNAPOS location & existence | 1 | 1 | 1 (notation suffix list wrong) |
| Part D ship-type chapters | 17 | 12 rows covered | 5 chapters with no catalog row (low priority) |
| Part E ship-type chapters | 12 | 6 rows covered | 6 chapters with no catalog row (Diving Support Vessels = high priority) |
| Part F additional-notation chapters | 16 | 7 cited correctly | 1 naming error (RP→AVM-DPS), 2 uncited relevant chapters (Ch.14 Electric Propulsion, Ch.15 Elastic Shaft Alignment) |

**Net assessment:** The catalog's core structural claims (which Part/Chapter/Section governs thrusters, steering gear, shafting, and its 8 cross-referenced rule notes) are all verified accurate against the live Jul 2026 edition. The issues found are all secondary: one wording precision error (≥110kW), two notation-naming errors (DYNAPOS suffixes, RP→AVM-DPS), and a ship-type coverage gap — most notably Diving Support Vessels, a thruster/DP-intensive vessel class with zero mention in the 15-row ship-type matrix.

---
---

# ROUND 2 — deep transcription of the actual submission tables (2026-07-16)

Round 1 (above) verified that the catalog's *structural* claims were right. Round 2 went
into the rule text itself and transcribed the **actual documentation tables**. The finding
is more serious than round 1: the catalog's document lists were **not** drawn from the rule
tables at all. They were plausible-sounding engineering lists with generic citations
("NR467 Pt C Ch.1"), and in several places they contradict the rule's own A/I categorisation.

`thruster-quickref.html` has been rebuilt so every line it emits is traceable to a named
rule table row or article. `Main.tex` still carries the older invented lists — see
"Outstanding" at the end.

---

## 7. ★ NR584 — the missing dedicated thruster rule note

**NR584 — "Azimuth thrusters in ice for polar class ships and icebreakers", Apr 2026.**

This is a complete, dedicated BV rule note for azimuth thrusters. **It is cited nowhere in
the catalog.** For a polar-class or icebreaker azimuth installation it is the controlling
document, and it is far more demanding than NR467 Sec 15.

- **Application [1.1.1]**: ships fitted with an azimuth propulsion system and assigned a
  service notation **icebreaker** or an additional class notation **POLAR CLASS**.
- **[1.1.2]** covers both **podded electrical thrusters** (steering unit, slewing bearing,
  rudder part, pod containing the electric motor) and **Z/L geared thrusters** (steering
  unit, upper gearing, lower gearing, nozzle, prime mover — diesel or electric).
- **8 sections**: Sec 1 General · Sec 2 Structure of the Thruster Body · Sec 3 Machinery
  Assessment · Sec 4 Electrical Installations · Sec 5 Steering Units · **Sec 6 Structural
  Assessment of the Thruster Body in Ice** · Sec 7 Tests · Sec 8 Certification.
- **Submission tables**: Tab 2 = **55 documentation items**; Tab 3 = solid propellers (4);
  Tab 4 = built-up and CP propellers (8); Tab 5 = manufacturer data (6).

Distinctive items with no equivalent anywhere in NR467 Sec 15, e.g.: *ice load calculation
of the thruster body* (#15), *stress calculation for the thruster body* (#16), *maximum
propulsive power in ice conditions as a function of steering angle and shaft speed* (#18),
*detailed drawing of the propeller shaft including the brake* (#20), *operation manual of
the thruster in ice conditions* (#11), *FMEA of the propulsion* covering cooling,
lubrication, ventilation, sealing, steering, control and fire safety (#5), *risk analysis of
hydraulic locking* (#55).

---

## 8. NR467 Pt C, Ch 1, Sec 15 — the real submission tables

Sec 15 [1.4] directs: athwartship and azimuth thrusters → **Tab 1 + Tab 2 + Tab 3**;
water-jets → **Tab 4**; manufacturer data → **Tab 5**. There are **five** tables, not three.

**A = to be submitted for approval · I = to be submitted for information.**

### Tab 1 — all thrusters (5 items)
| # | A/I | Documentation |
|---|---|---|
| 1 | **I** | General arrangement of the thruster |
| 2 | A | Propeller (incl. applicable details of Ch 1, Sec 8) |
| 3 | A | Bearing details |
| 4 | A | Propeller and intermediate shafts |
| 5 | A | Gears (incl. applicable details of Ch 1, Sec 6) |

### Tab 2 — transverse thrusters (4 items)
Structure of the tunnel (A, showing materials and thickness) · Structural equipment/connecting
devices transmitting thrust from propeller to tunnel (A) · Sealing devices (A — propeller
shaft gland and thruster-tunnel connection) · Pitch control device and monitoring system
(A — for adjustable pitch propellers).

### Tab 3 — rotating and azimuth thrusters (5 items)
Structural items (A — nozzle, bracing etc.) · Structural connection to hull (A) · Rotating
mechanism of the thruster (A) · Thruster control system (A) · Piping systems connected to
thruster (A).

### Tab 4 — water-jets (7 items)
General arrangement (**I**) · Casing/duct (A — location and shape, materials, thicknesses,
forces acting on the hull) · Details of shafts, flanges, keys (A) · Sealing gland (**I**) ·
Bearings (A) · Impeller (A) · Steering and reversing buckets, their control devices and
corresponding hydraulic diagrams (A).

### Tab 5 — manufacturer data, thrusters and water-jets (4 items)
Data on ratings (**I** — rated power, thrust and revolutions) · Material specifications of
the major parts (A) · Weldings (A — where of welded construction: joint design, procedures,
heat treatments, NDE after welding) · Background information on previous operating
experience (**I**, where applicable).

### Discrepancies against the catalog's invented lists
1. **General arrangement is I, not FA.** Catalog Table "General Requirements" #1 lists the GA
   drawing as **FA**. The rule categorises it **I** (Tab 1 #1, and Tab 4 #1 for water-jets).
2. **Technical specification sheet is I, not FA.** Catalog #2 lists it FA; the rule's
   equivalent is "Data on ratings" — **I** (Tab 5 #1).
3. **Water-jet sealing gland is I**, not FA (Tab 4 #4).
4. **Volume.** The rule requires 13 items for a tunnel thruster (Tab 1 + Tab 2 + Tab 5). The
   catalog's tunnel-thruster chapter lists ~39. The extra items are not wrong to *ask about*,
   but they are not rule-mandated submissions and must not be presented as though they were.

---

## 9. Scope definitions that change what is even in scope

- **[1.2.1] Thruster** — *"a propeller installed in a revolving nozzle or in a special
  transverse tunnel in the ship, or a water-jet… **Propulsion propellers in fixed nozzles are
  not considered thrusters** (see Ch 1, Sec 8, [1.1.1])."*
  → The catalog's "fixed nozzle (Kort-type)" configuration under thrusters is **out of Sec 15
  scope** when it is a propulsion propeller: it belongs to Sec 8. The rebuilt tool raises an
  explicit warning for this case.
- **[1.3.1]** — *"In general, at least two azimuth thrusters are to be fitted in ships where
  these are the sole means of propulsion. Single azimuth thruster installations will be
  specially considered."* Also applies to water-jets. Absent from the catalog.
- **[1.2.2]/[1.2.3]/[1.2.4]** define transverse thruster, azimuth thruster and water-jet.

## 10. Duty (manoeuvring vs propulsion) changes almost every technical requirement

| Aspect | Manoeuvring only | Propulsion / steering |
|---|---|---|
| Propeller | Sec 8 [2.5] **without** the 10% thickness increase — [2.2.2] | Sec 8 [2.5] in full |
| Shaft | formula in Sec 15 [2.2.3] (+10% at a keyed connection) | Ch 1, Sec 7, [2.2.3] |
| Gears | Sec 6 with **auxiliary** gear safety factors — [2.2.4] | Sec 6 with **propulsion** safety factors |
| Material tests | **need not** be Surveyor-witnessed if full reports provided — [3.1.2] | **witnessed by a Surveyor** — [3.1.1] |
| Ice class | **only** Pt F, Ch 8, Sec 3, [3.5.1] | full Pt F, Ch 8 |

The catalog has a "duty" concept but does not carry these specific rule consequences.

## 11. Other Sec 15 requirements not reflected in the catalog
- **[2.2.6]** tunnel thickness **not less than the adjacent part of the hull**; non-welded
  tunnel-to-hull connections specially considered.
- **[2.2.5]** nozzle structure → **Pt B, Ch 12**; nozzle-to-hull scantlings and weld type/size
  specially considered, detailed stress analysis may be required for high power installations;
  **for steerable thrusters the equivalent rudder stock diameter is calculated per Pt B, Ch 12**.
- **[2.3.2]** water-jet guide vanes / shaft supports: **fatigue strength calculation to be submitted**.
- **[2.3.3]** water-jet stator/rotor: **no natural frequency near the stator-rotor interaction
  excitation frequencies; calculations to be submitted** for maximum speed and any currently used speed.
- **[2.4.1]** steering thruster controls from **navigation bridge, machinery control station and
  locally**; means to stop any running thruster at each station; **thruster angle indicator at each
  steering control station, independent of the control system**.
- **Tab 6** minimum alarms for propulsion/steering thrusters: steering oil pressure **low**, oil
  tank level **low**. (Much shorter than the catalog's alarm expectations.)
- **[3.3.1]** thrusters **individually tested and certified**; **[3.3.2]** mass-produced units may
  go through the **type approval programme** instead.

---

## 12. NR467 Sec 14 — the steering-gear route for thrusters

- **[1.1.1]** Sec 14 applies to steering gear of all mechanically propelled ships **and to the
  steering mechanism of thrusters used as means of propulsion**.
- **Tab 1 #13** is the thruster entry: *"For azimuth thrusters used as steering means:
  Specification and drawings of the steering mechanism; where applicable, documents 2 to 6 and
  8 to 12 above."* — i.e. the thruster steering package is a defined **subset** of the steering
  gear table, not the whole of it. The rebuilt tool reproduces exactly that subset.
- **Article 4** is dedicated to ships with thrusters as steering means:
  - **[4.1.1]** the steering gear may consist of **azimuth thrusters, water-jets or cycloidal
    propellers** complying with Sec 15 — this is the rule basis for treating VSP as a steering means.
  - **[4.1.2]** two or more thrusters as steering means → control system must include
    **automatic synchronisation of thruster rotation**, unless each thruster withstands the
    others' forces.
  - **[4.2.3]** single steering-propulsion unit → 2+ steering actuating systems **and a detailed
    risk assessment to be submitted**.
  - **[4.2.5]** main steering: **≥ 2,3°/s** average turning speed at maximum ahead service
    speed, power operated for all ships, undamaged at maximum astern speed.
  - **[4.2.6]** auxiliary steering: **≥ 0,5°/s** at half maximum ahead service speed **or 7
    knots whichever is greater**; power operated where needed for SOLAS II-1/29.4.2 and in any
    ship with **> 2 500 kW per steering-propulsion unit**.
  - **[4.2.8]** where propulsion power **> 2 500 kW per thruster unit**, alternative power supply
    **automatically within 45 s**, capacity **≥ 30 min** for ships ≥ 10 000 GT, **≥ 10 min** otherwise.
  - **[4.3.1]** use of **water-jets as steering means will be given special consideration**.

None of these numeric criteria appear in the catalog.

---

## 13. Electrical — Pt C, Ch 2

- Sec 15 **[2.2.1]** sends electric thruster motors **and their feeding systems** to
  **Pt C, Ch 2, Sec 4** (Rotating Machines), with two express provisions: prevent starting
  whenever there are insufficient generators in operation; intermittent duty thrusters
  specially considered.
- **Ch 2, Sec 4, Article 5 — "Additional tests for rotating machines used as propulsion motor
  or thruster"**: for machines **developing more than 1 MW**, during assembly — shaft line per
  Ch 1 Sec 7; rotor dynamic balancing; stator dielectric + insulation resistance after
  impregnation; frame visual + **liquid penetrant test of 10% of structure welds and 100% of
  handling points**; watercooler visual + performance test; hydrostatic jacking unit pressure
  and working tests.

The catalog's electric-drive list (VFD spec, harmonic study, cable segregation etc.) is
reasonable engineering practice but is **not** what Sec 15 [2.2.1] actually cites.

---

## 14. DYNAPOS — Pt F, Ch 11, Sec 5

Full 22-row documentation table transcribed into the tool. Key correction:

> **Item 17, Failure Mode and Effect Analysis (FMEA), is annotated "For symbols R and RS only".**

[2.4.1] confirms: *"For installation intended to be assigned the notation DYNAPOS AM/AT R and
DYNAPOS AM/AT RS an FMEA is to be carried out."* **Plain DYNAPOS AM, AT or AM/AT does not
attract an FMEA.**

The catalog states the opposite in its disclaimers — *"For DP systems, the FMEA is the
cornerstone document. Inadequate FMEA is grounds for rejection"* — presented unconditionally.
That is wrong for AM/AT-only installations. The tool now gates the FMEA on an explicit R/RS
selection and explains the gate.

Also thruster-specific in that table: **#11** layout drawings of thrust units, thrust shafts
and blocks, arrangement of hull passages, thrust curves of each propulsion unit; **#18** study
of possible interaction between thrusters; **#3** capability plots including the worst case failure.

DYNAPOS **[1.1.3]** cross-refers to Pt C, Ch 1, Sec 2 (engine-driven thrusters), **Pt C, Ch 1,
Sec 15** (azimuthal and transverse thrusters) and Pt F, Ch 3 (automation).

---

## 15. Ice class — the single most over-scoped area in the catalog

**Pt F, Ch 8, Sec 3, [3.5.1] in full, verbatim:**

> **"Tunnels of transverse thrusters are to be fitted with grids for protection against ice impacts."**

Sec 15 **[1.1.1]** states that transverse thrusters intended for manoeuvring on ICE CLASS ships
*"are required to comply with additional requirement Pt F, Ch 8, Sec 3, [3.5.1] only"*.

**One sentence. One grid.** The catalog's Ice Class chapter applies an ice-strengthening
submission set (propeller ice-load strength calculation, shaft/gear ice-torque verification,
lower-unit/slewing ice-block impact, winterisation, low-temperature material certification) to
thrusters generally. For a bow tunnel thruster on an ICE CLASS ship that is a substantial
over-demand. The tool now splits the two paths and raises an explicit "do not over-scope" warning.

By contrast, thrusters for **propulsion and steering** on ICE CLASS ships do get the full
Pt F, Ch 8, Sec 3 Article 1 treatment, including **[1.11] azimuthing thruster body** — extreme
ice impact loads, ice loads penetrating an ice ridge, thruster body global vibration,
**steering gear design torque in ice**, and protection of the steering gear against excessive torque.

**Ice notations (Pt F, Ch 8, Sec 1, [1.1.1])** are: ICE CLASS **IA SUPER, IA, IB, IC, ID**,
**YOUNG ICE 1**, **YOUNG ICE 2**. The catalog lists only IA SUPER/IA/IB/IC — missing ID and both
YOUNG ICE notations. [1.1.2] notes the strengthening requirements (excepting ID, YOUNG ICE 1 and 2)
are equivalent to the **Finnish-Swedish Ice Class Rules 2019, as amended**.

POLAR CLASS / icebreaker propulsion-and-steering thrusters → **NR527**, and for azimuth systems
→ **NR584** (§7).

---

## 16. The wider BV publication landscape by ship type

Rules Explorer carries **7 Main Rules, 68 Rule Notes, 57 Guidance Notes, 15 Former**. Governing
publication by unit type:

| Ship / unit type | Governing publication | Edition |
|---|---|---|
| Sea-going steel ships (default) | **NR467** | Jul 2026 |
| Naval ships | **NR483** | Dec 2025 |
| FSRU / FSU | **NR645** | Dec 2025 |
| Inland navigation vessels | **NR217** | Jun 2025 |
| Offshore units (MODU) | **NR445** | Jun 2025 |
| Yachts | **NR500** | Oct 2024 |
| High-speed craft | **NR396** | rule note |
| Ships < 500 GT | **NR566** (+ NR600 hull) | Nov 2024 |
| Polar waters / icebreakers | **NR527** | Jan 2026 |
| Diving systems (on a DSV) | **NR610** — *prevails over NR467 for the diving system, per Pt A, Ch 1, Sec 1, [1.1.3]* | — |
| Materials and welding (all) | **NR216** | Jan 2025 |

Other rule notes relevant to thruster packages and **not cited in the catalog**: **NR584**
(azimuth thrusters in ice), **NR659** (cyber security), **NR674** (condition monitoring —
relevant to MON-SHAFT), **NR614** (underwater radiated noise), **NR632** (hardware-in-the-loop
testing — DP/control validation), **NR598** (safe return to port — the catalog cites only SOLAS),
**NR656** (power generation units), **NR526** (lifting appliances). Guidance notes: **NI663**
(propeller in composite materials), **NI543** / **NI565** (ice selection and ice/structure
interaction), **NI649** (lay-up and reactivation of DP vessels).

---

## 17. IACS and SOLAS (verified off Rules Explorer)

- **IACS UR I3 — "Machinery Requirements for Polar Class Ships"** covers propeller-ice
  interaction loads for **azimuthing and fixed thrusters**, geared and podded propulsors;
  propulsion machinery type factor **k3 = 1,0 fixed / 1,2 azimuthing**. Rev.2 CR in force 1 Jul 2024.
- **IACS UR E26 (Cyber Resilience of Ships)** and **UR E27 (Cyber Resilience of On-board Systems
  and Equipment)** — mandatory for ships **contracted on or after 1 July 2024**. The catalog
  mentions cybersecurity but gives no threshold date.
- ⚠️ **UR M78 is "Internal Combustion Engines Fuelled by Gases or Low-flashpoint Fuels"** — it is
  **not** a thruster requirement. Do not cite it in thruster work.
- **SOLAS II-1/29.4.2** is cited by NR467 Sec 14 [4.2.6]; **IMO Res. MSC.137(76)** (Standards for
  ship manoeuvrability) governs the manoeuvrability trials referenced in Sec 14 Article 4, to be
  run at steering angles not exceeding the declared steering angle limits.

---

## 18. What was rebuilt, and what is still outstanding

**Rebuilt — `thruster-quickref.html`.** Every emitted line now carries an exact citation
(e.g. "NR467 Pt C, Ch 1, Sec 15, Tab 1 #2"), uses the rule's own **A / I** categorisation, and
is grouped by its source table so provenance is visible. Added: the five Sec 15 tables, the
Sec 14 Tab 1 #13 subset, the DYNAPOS table with R/RS gating, the split ice paths, the full
NR584 tables, a "rule verification checks" panel carrying the numeric criteria (2,3°/s, 0,5°/s,
45 s, 30/10 min, 110 kW, 1 MW, 2 500 kW), scope warnings (fixed-nozzle exclusion, ice
over-scoping, <110 kW), and ship-type → governing-publication mapping for 24 ship types.
Tested across 108 type × duty × ice combinations with no errors.

**Outstanding — `Main.tex` / `Main.pdf`.** The PDF catalog still contains the pre-rule-table
document lists, the GA/spec-sheet FA mis-categorisation, the unconditional DP-FMEA statement,
the over-scoped ice chapter, and no reference to NR584. Bringing the PDF in line with the
transcribed tables is a larger edit than the v1.7 corrections and has not been done.
