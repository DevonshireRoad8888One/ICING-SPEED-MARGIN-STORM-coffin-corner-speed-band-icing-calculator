Final state
Repository
coffin-corner-calculator
README
README.md at the root — the only name GitHub reliably renders
Calculator
release/v2.6-r1/coffin-corner-calculator-v2.6-r1.html
Digest
1e9771a4b40309c2b578156025052d582eca7b0f60d00a33f6925ed4e79e89e8
Bytes
110 211
Checks
83/83, browser-verified 2026-11-10
Build history
BUILD_HISTORY.md — every build, every defect, every digest
Licence
LICENSE — MIT for the code, explicit carve-out for the aviation content


Sierra 7 out.

# Coffin Corner — Icing, Speed Margin & Storm Calculator

> **EDUCATIONAL STUDY AID — NOT FOR FLIGHT OPERATIONS.**
> Not approved aircraft performance. Not certified margins. Not a dispatch tool.
> Not an operating clearance. Never use its outputs to make real-time flight decisions.
> Use current AFM/POH data, aircraft-specific airspeed corrections and approved procedures.

A **single-file, offline, zero-dependency** HTML calculator for high-altitude speed-band
management: stall margin, overspeed margin, dynamic pressure *q*, icing penalty and a
margin-policy verdict — with a piston mode for single-engine aircraft, an ADS-B dive
reconstruction tab, and the N722BD case material as teaching material.

Open the file. Nothing installs, nothing phones home, nothing is stored.

---

## Current release — v2.6 r1

| | |
|---|---|
| **File** | `release/v2.6-r1/coffin-corner-calculator-v2.6-r1.html` |
| **SHA-256** | `1e9771a4b40309c2b578156025052d582eca7b0f60d00a33f6925ed4e79e89e8` |
| **Bytes** | 110 211 (artefact of record, CRLF) |
| **Self-test** | `SELF-TEST PASS 83/83` — verified in a real browser, 2026-11-10 |
| **Dependencies** | none |
| **Network calls** | none |

---

## Quick start — 30 seconds, fully offline

1. Take `release/v2.6-r1/coffin-corner-calculator-v2.6-r1.html` from this repository (or
   from the GitHub release) and open it. It runs from `file://` — no server, no install,
   no internet.
2. Read the two stamps under the title bar:

3. Open **REFERENCE & TESTS** and press **Run all self-tests** — 83 rows, all PASS.
4. Pick **Mode**: **JET** (Mach / MMO envelope, high altitude) or **PISTON** (IAS stall
   margin only — no coffin corner for a normal-category piston).
5. The tool opens on the published N722BD Case 1, so the **ENVELOPE** and **CASE STUDY**
   tabs agree.

---

## Verifying the release

The checksum is the identity of the file. Verify it before you trust a number.

```powershell
# one-liner, run from the release/v2.6-r1 folder
(Get-FileHash -Algorithm SHA256 .\coffin-corner-calculator-v2.6-r1.html).Hash.ToLower()

# or use the bundled report, which also checks the file's content and offline properties
.\verify_release.ps1
.\verify_release.ps1 -Archive     # also writes VERIFICATION-<timestamp>.txt
README.md                                  this file
BUILD_HISTORY.md                           every build, every defect, every digest
LICENSE                                    MIT for the code + aviation-content carve-out
release/
  v2.6-r1/
    coffin-corner-calculator-v2.6-r1.html   the calculator (one file, offline)
    SHA256SUMS.txt                          the release digest
    RELEASE_NOTES.md                        what changed and why
    verify_release.ps1                      verification report
    deploy_v2_6_r1.ps1                      installs the byte-exact artefact
tools/
  make_v2_6_release.ps1                     rebuilds v2.6 from the v2.5 base
  patch_v2_6_r1.ps1                         rebuilds v2.6 r1 from v2.6
  verify_v2_6_release.ps1                   independent release gate
docs/
  case-notes.md                             the working case file and correction log
  v2.x-changelog.md                         per-build change notes

---

# FILE 2 — `BUILD_HISTORY.md` (repository root)

```markdown
# Build history — Coffin Corner

Every build, in order, with what it changed, what it cost in checks, how it was
verified, and where it stands. The full defect record — including the defects the
suite found in the suite's own new code — is in `docs/case-notes.md` §11 and in each
`docs/v2.x-changelog.md`.

---

## Summary

| Build | Checks | Built from | Verified in a browser | Status |
|---|---|---|---|---|
| v2.1 | — | rewrite | no | superseded — root correction |
| v2.2 | 48 | v2.1 | no | superseded |
| v2.3 | 55 | v2.2 | **yes — 55/55, 2026-11-08** | superseded — known-good fallback |
| v2.4 | 67 | v2.3 | **yes — 67/67, 2026-11-10** | superseded — **carries the stall-TAS display defect** |
| v2.5 | 70 | v2.4 | no | superseded — base for the release chain |
| v2.6 | 83 | v2.5 | **yes — 82/83, 2026-11-10** | superseded — one guard failed |
| **v2.6 r1** | **83** | v2.6 | **yes — 83/83, 2026-11-10** | **RELEASED** |

---

## v2.1 — the root correction

**What changed.** The metres-per-second → knots and → mph factors were wrong; they were
not conversions at all. The sound speed was scaled by 15 %, and every Mach-derived number
with it. Corrected: sound speed at FL350 is **576.4 kt** (663.4 mph), not 500.5 kt, and
`a·√σ` at FL350 is **320.9 kt**, not 278.9 kt.

**What it changed in the published case.** The earlier "0.87 kt policy window" claim for
the N722BD top of climb was an artefact of that error. The true figures are a **34.8 kt
policy window**, a **+38.9 kt stall margin** at +10 % ice, and a margin that does not
reach zero until **31 % ice accretion**. The band for this airframe closes near
**FL433**, not FL415.

Also in v2.1: generic IAS labels replaced with EAS; explicit KCAS handling for VMO;
CLmax degradation separated from ice coverage; per-configuration stall data made
editable; blank-input handling corrected and required inputs made to fail visibly;
policy-window closure reworked to include both the stall and the overspeed buffer; thedive logic corrected (groundspeed + vertical speed is ground-relative, not TAS; GPS
altitude separated from pressure altitude; sparse-data impact speed and G-force
extrapolation removed; recovery commands replaced by non-operational regime
classifications).

---

## v2.2 — features

Piston mode (IAS stall margin, piston icing hazards). The DIVE pressure-altitude
cross-check, which exposes the frozen pressure-altitude field in the N722BD final report.
Eight-tier evidence table. Per-configuration stall data with evidence tier and source
reference. User-defined storm buffers. Wind-aware dive reconstruction.

**Checks: 48.** Not executed in a browser at the time.

---

## v2.3 — three real corrections

1. **The mandatory `+1`.** The supplied v2.2 printed `M_CAS = √(5[(qc/p₀)^(2/7) − 1])`.
   The correct relation is `M_CAS = √(5[(1 + qc/p₀)^(2/7) − 1])`. As printed, the bracket
   is negative for every realistic calibrated airspeed, so the expression returned NaN.
   The corrected form is pinned by a round-trip test plus a check that the old form is
   not finite.
2. **One degradation convention.** The stall degradation had been ambiguous — a base
   speed already carrying a CLmax loss, multiplied again by an ice percentage, against a
   separate CLmax-loss input. Three mutually exclusive conventions were introduced:
   **A** aerodynamic, **B** legacy ice heuristic, **C** ice mapped to CLmax, with the
   equivalence stated: `143.3 × 1/√(1 − 0.40) = 185.00` exactly, and +10 % ice on the
   185 reference equals a 17.36 % CLmax loss — 50.41 % in total against the 143.3 clean
   reference.
3. **Strict airspeed labels.** EAS, KEAS, KCAS and KIAS used separately and consistently.
   The proxy treatment of a KIAS-derived figure as a KEAS input is disclosed where it
   applies.

Also: the hard-coded storm minimum removed; recovery material reduced to classification
only; the tropopause pressure taken continuously from the troposphere formula; dynamic
pressure corrected from a knots-based to an SI computation; the EAS identity check
corrected (it had compared a knots value against an SI identity, so it could never pass).

**Checks: 55. Browser-verified 2026-11-08 — 55/55.** Known-good fallback.

---

## v2.4 — restore and disclose

The speed-band indicator and the editable per-configuration stall table — both dropped by
the v2.3 rebuild — were restored. The Copy brief action was added. The CLmax-table
wording was corrected (it had said "clean reference" when the reference may already carry
a CLmax loss).

**Checks: 67. Browser-verified 2026-11-10 — 67/67.** The same run exposed a defect:

> **The "Stall (modelled)" TAS cell divided EAS by σ instead of √σ** — a factor of 1.837.
> It printed **686.9 kt** where the physics gives **373.9 kt**: faster than the 474.7 kt
> ceiling TAS on the same page, at a *lower* Mach, at the same altitude where the speed
> of sound is a single number. Impossible, and visible on the page. One display cell; no
> physics depended on it. Present in v2.3 and v2.4.

**Retained as the known-good v2.4 fallback, with the defect documented.**

---

## v2.5 — the √σ fix and the guards that would have caught it

The stall-TAS cell corrected to `EAS/√σ`. The CLmax-table columns relabelled ("Current
margin" → "Margin at this CLmax loss"; "User-buffer interval" → "Buffer interval at this
loss"), because the margin column of that sweep is *not* comparable with the headline
margin when an ice convention is active. The two brown caution zones named explicitly.
The relation `TAS = EAS/√σ` stated in the equations panel.

**Three regression guards were added — and the important part is how they are written.**
They read the **rendered DOM**, not the formulas, because a formula-level assertion
cannot see a display defect:

1. the rendered stall TAS cell equals stall `EAS/√σ` — an **exact string comparison**;
2. the rendered stall TAS agrees with the rendered stall Mach and the local speed of
   sound, `TAS = M·a` — state-independent, and it catches dividing by σ, by σ²,
   multiplying, or transposing columns;
3. when the current EAS is above the modelled stall, the stall point must be a slower
   condition than the present state.

**Checks: 70.** Not executed in a browser at the time — this is why the defect was
caught in the *next* build's run rather than here.

---

## v2.6 — the deployment review

**Visible wording brought inside the tool's own evidence discipline.** `SAFE` → `BUFFERED`.
`DANGER` → `OUTSIDE BAND`. `ABOVE THE OPERATING LIMIT` → `ABOVE THE MODELLED CEILING`.
`NO COMPLIANT SPEED` → `NO USABLE SPEED BAND`. The verdict colour class `go` renamed `ok`,
so the token GO appears nowhere in the source.

**One status stamp became two.** The build stamp reports the software only. A second
input-state stamp reports validation errors, advisory notes and the evidence tier, and is
**never rendered in the green state**. The green build stamp therefore cannot appear
alongside a failed or warning state.

**The suite was pinned to a fixture** (JET, FL35250, ISA, convention A, +10 % ice, M0.76,
27 500 lb, 10/10 buffers) and restores the user's inputs afterwards, so the stamp no longer
turns red when the user changes inputs or switches to PISTON mode.

**Two false greens closed.** An EAS above the user's buffered ceiling — inside the raw
aerodynamic interval, in the tool's own brown caution zone — was being reported as "WITHIN
THE USER BUFFER" in green; it is now reported as caution. And a hard validation failure
could no longer leave a positive verdict on screen.

Also: convention C disclosed as algebraically identical to convention B, with a guard
pinning the identity; `esc()` taught to escape quotes; the exported brief made to state
the computed ISA temperature instead of a fixed string; the ice table taught to highlight
the entered ice percentage and to state that it is a Convention B sweep and **not the
model in force**; and the tool made to open on the published N722BD case so the ENVELOPE
and CASE tabs agree.

**Checks: 83. Browser-tested 2026-11-10 — 82/83.** The failing check was the tool's own:

Both scripts abort without writing if any anchor fails to match exactly once, so the
chain is derived rather than transcribed. `verify_v2_6_release.ps1` is the independent
gate: it does not trust the builder.

---

## Standing weaknesses, recorded not fixed

1. **Five checks are self-referential** — wind correction, vertical wind, derived vertical
   rate, PA-staleness threshold, and the no-GO/NO-GO source scan. They certify
   documentation, not behaviour, and cannot fail if the formula drifts.
2. **The CLmax guard is a warning, not a hard stop.** The stall factor clamps loss to
   0.9999, so a bypassed warning would yield a 10× stall speed rather than a refusal.
3. **PISTON mode reuses the Mach field as IAS**, and the field keeps its value across a
   mode switch — a stale IAS can be carried silently.
4. **No persistence.** Configurations, tiers, source strings and dive points are lost on
   reload. A `localStorage` save plus JSON export/import is the highest-value addition.
5. **The dive "3D TAS" resolves the along-track wind only**; a crosswind is not resolved.
6. **Case-tab rows marked MEASURED carry no source citation.** An NTSB report number and
   date on those rows would make the evidence discipline internally consistent.
7. **The track's knot scale stops at 250** while the axis runs to 284 — the right-hand
   12 %, including the whole outside-the-band zone, has no scale reference beneath it.
8. **The ice table labels negative-margin rows "MARGIN REACHED ZERO"** — true, but
   imprecise next to the single zero-crossing row.
