# BV Rules Explorer Verification Log

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
