
Why this tool exists

We fly a profession where the margin between a good day and a bad outcome is built out of a hundred small things done properly. And we fly it knowing the margin is thinner than it looks — and that the people who found out how thin it was are the reason we know it at all.

Learjet 60, N722BD, near Military Trail and 10th Avenue North in Palm Beach County, Florida — 1 November 2026. Nine souls.

Captain Jeff Gregory and First Officer Nathalia Gadelha Filgueiras. Seven passengers: a founder, his wife, their two young children, their nanny, and two family friends.

That accident is why this tool exists, and it exists for one reason.

I want to save future pilots' lives. That is the whole of it. Everything else in this file is in service of that, and nothing else.

Here is what I know about how that happens. The margin in an accident is not one number; it is a chain of them, each one small, and the accident lives in the chain rather than in any single link. Nobody in that aeroplane was overcome by one spectacular failure. They were overtaken by a series of ordinary margins that had all been a little smaller than they needed to be, and every one of them was individually survivable. That is what makes those accidents so hard to learn from and so easy to repeat: nothing in the chain looks like a cause. You cannot point at one link and say there. You have to hold the whole chain at once and see where it thinned.

I could not hold it in my head. So I built something that holds it. The tool reconstructs the atmosphere the aircraft was actually in — not an idealised one — and asks the questions that were live in that aeroplane at 35,250 feet in minus forty-seven degrees: how much stall margin was really left, what the speed was against the ceiling, what the air was doing to the wing, what could and could not have been done in the seconds that were available. It is deliberately slow and deliberately explicit, and it will not tell you a cause it cannot support. The case study inside it is labelled the way it has to be: a hypothesis and teaching material, not a finding, and not independently verified 
v2.6 r1 - Storm...7 (1).html
.

But the tool is not for the dead. It is for the ones still coming.

That is the part I want to be unambiguous about, because the file can look like a memorial and it is not. Run it for your aeroplane, your weight, your icing scenario, your altitude and see the margin you are actually flying with, on the day, in the conditions you actually fly in. Run it for the configuration you are certified for — and then for the configuration you are about to be asked about. Run it with the number you assumed, and then with the number that was true.

That is how this saves lives. Not by explaining a crash that has already happened — though understanding one is the price of the tool — but by putting the margin in front of people before it is the margin that matters. A pilot who has watched, in a quiet room, how little stall margin a given weight and a given condition actually leaves, is a pilot who will recognise what he is looking at in the cockpit when the day turns. A company that has done that arithmetic can build a procedure around the real number instead of the comfortable one. An instructor can show a student the edge, and the edge is worth far more to a student than a rule.

Why it had to be a tool and not a document. Because the numbers will not sit still in prose. The atmosphere at altitude is not a feeling, it is a reconstruction, and it has to be computed in the right units, at the right altitude, with the right temperature. And because the data is scattered across a report, an FDR, a radar, a sounding, a crater and a set of procedures, and no single person is going to hold all of it. So: gather it, compute it, put it somewhere it can be questioned — and let more than one set of eyes at it, because the failure mode of an investigation is not bad arithmetic, it is one mind that got attached to its own answer. That is why the file's case study is explicitly a hypothesis and not a finding 
v2.6 r1 - Storm...7 (1).html
, and why its competing mechanisms — icing degradation, autopilot interaction, transonic effects, structural failure, air-data inconsistency — are set out for testing and deliberately not ranked 
v2.6 r1 - Storm...7 (1).html
. A tool that decides for you is worse than no tool, and a finding nobody has tested is an opinion with a citation.

To the pilots who are not with us any more. All of them, in every company, in every country, in every year. You are the reason the margin exists at all. Every procedure that exists because someone died for not having it, every checklist line that is there because a crew had a bad day, every training manoeuvre that is drilled because the alternative is written on a stone — that is your work, and it outlasts you. If some of it ends up inside a tool like this one, you are still working.

And it was not only the crew. A person on the ground was injured, and some six hundred neighbours were displaced from their homes. They are part of what happened too, and they are part of why the margin is worth protecting.

To the families. I cannot speak for an investigation and I will not try. What I can say is that the people who fly have not forgotten, and that the work of understanding — done carefully, by more than one set of eyes, without claiming more than the evidence supports — is one of the ways we say so.

And to whoever is reading this because they are about to do the same analysis I did. You are not the first. That is the point of the tool. Use it, argue with it, make it better, and teach the margin to somebody who has not thought about it yet. When the numbers will not sit still, that is the data telling you something, not a failure of the method.

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

---Zulu 7, Sierra 7 — good catch, and the answer is: the green is correct, but it is worth understanding exactly what it is asserting.

1. First, a correction of the premise: the table itself is not green
In the Speed-envelope comparison table, the highlighted Stall margin row is tinted blue, not green. The green you are seeing belongs to the speed-band indicator immediately above that table — the green span of the track — and it appears in three other places on the ENVELOPE tab 
v2.6 r1 - Storm...7 (1).html
:

WHERE
WHAT IS GREEN
WHAT IT ASSERTS
Track, the green span
the buffered interval
the current EAS sits inside both of your buffers
Verdict tile
WITHIN THE USER BUFFER
the same statement, in words
Result tile — Stall margin 38.9 kt
the margin number
margin ≥ your 10 kt buffer
Result tile — Policy window 34.9 kt
the window number
the buffered band is open


All four are one single claim: your 242.4 kt EAS is above the floor of 213.5 kt and below the ceiling of 248.4 kt — so the margin is +38.9 kt and the window is 34.9 kt. Nothing else.

2. Why this is not a false green
Because the green is a qualified statement, and the qualification is printed in the same block. The row directly above the highlighted one says what the buffers are; the banner above that says these are user-defined study values, not approved operating margins and not regulatory limits 
v2.6 r1 - Storm...7 (1).html
.

So read it in this order:

green → relative to thresholds you typed yourself — an arithmetic comparison.
amber stamp → can these numbers be trusted as certified performance? — an evidence judgement.

Those are two different questions about the same card, and v2.6 deliberately kept them on separate channels. That separation is the deployment review: the build stamp reports the software, the input-state stamp reports the evidence, and the colours in the Result card report the comparison you asked for.

The rule you had me enforce is intact. With the shipped ILLUSTRATIVE presets the build stamp is amber, never green, and the input-state stamp is amber too. The green belongs to the arithmetic, not to the build. If the stamp could turn green here, that would be the defect — and it cannot.

3. The one thing I would flag, because it is a judgement call and not physics
In one visual field, green means "good" to most readers. A quick glance at a green 38.9 kt sitting beside an amber stamp can read as an operational clearance, even though every string around it qualifies it. The v2.6 review fixed the words on the track — SAFE → BUFFERED, DANGER → OUTSIDE BAND — but left the colour on the verdict tile and the two Result numbers untouched.

That was deliberate: the arithmetic is sound, the evidence warning lives in its own channel, and making every number amber in the default preset would blur the signal. But it is a choice, not a law.

If you want colour to track evidence as well, the change is small and surgical: make the verdict tile and the Stall margin / Policy window tiles amber instead of green whenever the selected configuration's tier is not CERTIFIED or TYPE-DATA. Green then becomes a positive claim about documented data — reachable only with a certified stall reference — and it costs one line in renderEnv() plus one guard test.

Say the word and I will write it as v2.7, with the guard, and with the correction-log entry. It is a five-minute change to the code and it is the only remaining place where the tool's colour vocabulary is looser than its wording.

4. Nothing regressed
This behaviour is identical in the browser-verified build of 10 November and in the published v2.6 r1. The √σ fix changed one cell in the atmosphere table — 686.9 → 373.9 kt — and touched no colour logic. The figures you are reading now, 203.5 / 258.4 / 213.5 / 248.4 / M0.6693 / M0.7786 / 242.4 / 38.9 / 34.9, are the ones that were independently re-derived and reconciled before release.

Short answer: the green means inside your own buffers, the amber means not certified data, and both are correct at the same time. If the green on the numbers still bothers you, the one-line v2.7 above makes green mean certified — which is the stricter, more honest arrangement, and the one I would prefer if this tool is ever handed to a student who has not yet internalised the distinction between a green number and an approved one.

Sierra 7 out.

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

Coffin Corner — Icing, Speed Margin & Storm Calculator
EDUCATIONAL STUDY AID — NOT FOR FLIGHT OPERATIONS.
Not approved aircraft performance. Not certified margins. Not a dispatch tool.
Not an operating clearance. Never use its outputs to make real-time flight decisions.
Use current AFM/POH data, aircraft-specific airspeed corrections and approved procedures.

A single-file, offline, zero-dependency HTML calculator for high-altitude speed-band
management: stall margin, overspeed margin, dynamic pressure q, icing penalty and a
margin-policy verdict — with a piston mode for single-engine aircraft, an ADS-B dive
reconstruction tab, a storm-distance study tool, recovery-regime classifications and the
N722BD case material as teaching material.

Nothing to install. No server. No network calls. Nothing is stored.

Current release — v2.6 r1
File
release/v2.6-r1/coffin-corner-calculator-v2.6-r1.html
SHA-256
1e9771a4b40309c2b578156025052d582eca7b0f60d00a33f6925ed4e79e89e8
Bytes
110 211 (CRLF line endings)
Checks
83, all PASS
Verified
real browser, 2026-11-10, cold first load
Dependencies
none
Network calls
none


Digests for every build: release/v2.6-r1/SHA256SUMS.txt.
What changed in this release: release/v2.6-r1/RELEASE_NOTES.md.

Quick start
Download release/v2.6-r1/coffin-corner-calculator-v2.6-r1.html and open it. It runs
straight from file:// — no server, no install, no internet.
The header reads:

Collapse
Save
Copy
1
2
3
4
COFFIN CORNER - ICING, SPEED MARGIN & STORM CALCULATOR
v2.6 r1
BUILD v2.6 r1 | SCRIPT OK | SELF-TEST PASS 83/83 | INPUT STATE HAS ADVISORY NOTES
INPUT STATE: ADVISORY NOTES (2) - READ BEFORE USE | EVIDENCE TIER: ILLUSTRATIVE | NOT AN OPERATING CLEARANCE
Four tabs: ENVELOPE, DIVE DATA, CASE STUDY, REFERENCE & TESTS.
Pick Mode — JET (Mach / MMO envelope, high altitude) or PISTON (IAS stall
margin only; no coffin corner for a normal-category piston).
The tool opens on the published N722BD Case 1, so the ENVELOPE and CASE STUDY tabs
agree with each other.
Note: GitHub displays .html files as source, not as a running page. Download the
file and open it locally, or use a Pages link if one is published.

Confirming the 83/83 self-test
The suite runs itself when the page loads. To re-run it at any time:

REFERENCE & TESTS → Run all self-tests

The table then lists 83 rows, every one PASS. The count is derived at runtime and
can never drift from the number of checks actually executed. The panel says so itself:

The count is derived at runtime and can never drift from the number of checks actually
executed. The suite is the specification: changing a physical constant or a unit factor
requires changing the matching check in the same commit. PASS and FAIL here describe the
execution of a software check only - they are not a flight-safety assessment and carry no
operational authority.

Expected stamp after a run:


Collapse
Save
Copy
1
BUILD v2.6 r1 | SCRIPT OK | SELF-TEST PASS 83/83 | INPUT STATE HAS ADVISORY NOTES
Three optional exercises that test the deployment-review guards. Each must end in the
stated state — none of them is a failure:

ACTION
EXPECTED
Mode → PISTON, then Run all self-tests
The stamp still reads SELF-TEST PASS 83/83 — it must not turn red. The suite runs against a pinned fixture and restores your inputs afterwards.
Clear the stall reference field
The verdict turns red: INPUT ERROR - RESULT NOT VALID. The build stamp goes amber: INPUT STATE HAS A VALIDATION ERROR. The input-state stamp goes red.
Set Mach to 0.79
The verdict turns amber: ABOVE THE USER BUFFER, BELOW THE MODELLED CEILING — not green.


Verifying the checksum — SHA256SUMS.txt
SHA256SUMS.txt records the digest of the artefact of record: the released file, in
its CRLF form, 110 211 bytes.


Collapse
Save
Copy
1
1e9771a4b40309c2b578156025052d582eca7b0f60d00a33f6925ed4e79e89e8  coffin-corner-calculator-v2.6-r1.html
Step 1 — the plain, byte-exact check
From the release/v2.6-r1 folder:

powershell

Collapse
Save
Copy
1
(Get-FileHash -Algorithm SHA256 .\coffin-corner-calculator-v2.6-r1.html).Hash.ToLower()
Expect:


Collapse
Save
Copy
1
1e9771a4b40309c2b578156025052d582eca7b0f60d00a33f6925ed4e79e89e8
Step 2 — the bundled verification report
powershell

Collapse
Save
Copy
1
2
.\verify_release.ps1
.\verify_release.ps1 -Archive     # also writes VERIFICATION-<timestamp>.txt
verify_release.ps1 hashes the CRLF-normalised form, so it validates the released
artefact and any LF copy of identical content — which is why it passes even if your
editor re-saved the file with Unix line endings. It also asserts:

the byte length, and reports the line-ending style;
the presence of the √σ stall-TAS fix;
the absence of the old EAS/σ cell;
the 83-check count;
exactly one inline <script> tag, one <body> and one </html>;
and that the file contains no external reference and no network API of any kind —
no src=, href=, <link>, <img>, <iframe, @import, fetch(,
XMLHttpRequest, sendBeacon, WebSocket, importScripts, new Function, eval(,
http:// or https://.
Exit code 0 = pass, 1 = fail.

Step 3 — install the byte-exact artefact and regenerate SHA256SUMS.txt
If the file you hold is an LF copy, its raw digest differs from the one above even though
the content is identical. Put the released bytes in place and regenerate the sums file
from whatever is actually present:

powershell

Collapse
Save
Copy
1
.\deploy_v2_6_r1.ps1 -Archive
It verifies the source digest before copying, installs the file byte-exact, rewrites
SHA256SUMS.txt from the file that is now in the folder, and then runs the verification
report.

The two status stamps — and why the build stamp is amber
The build never hides a problem behind a green light.

STAMP
REPORTS
COLOUR
#stamp
The software only: BUILD v2.6 r1 | SCRIPT OK | SELF-TEST PASS 83/83. Green only when the suite passed and the input state carries no warning.
amber / red / green
#stateStamp
The input state: validation errors, advisory notes, evidence tier. Ends with NOT AN OPERATING CLEARANCE.
never green


With the shipped ILLUSTRATIVE presets the build stamp is amber, and that is the
intended state: the tool is telling you its own data is not certified. Green is reserved
for a configuration whose stall reference is CERTIFIED or TYPE-DATA with no validation
error — a state this tool's presets cannot reach, and must not fake.

The suite status has four states, not two: RUNNING while the checks execute, PASS
or FAIL once they have, and NOT RUN before the first execution. The stamp never claims
a failure it has not observed.

What the model computes
Atmosphere — layered ISA: troposphere to 11 000 m, isothermal above, with the
tropopause pressure taken continuously from the troposphere formula. Pressure from
pressure altitude; density and speed of sound from the supplied static air
temperature.
The identity that matters — EAS = M·√σ, so TAS = EAS/√σ, never EAS/σ.
EAS at a fixed Mach and pressure altitude is independent of temperature; Mach derived
from a measured TAS is not.
Calibrated airspeed — M_CAS = √(5[(1 + qc/p₀)^(2/7) − 1]). The +1 is mandatory;
without it the expression is NaN for every realistic airspeed. The round trip is pinned
by the suite.
Ceiling and speed band, as the tool's own equations panel states them 
v2.6 r1 - Storm...7 (1).html
:

Collapse

Run
Save
Copy
1
2
3
4
5
6
Upper Mach = min(MMO_effective, Mach_from_VMO)
Lower = (Vs_degraded + stall buffer) / (a sqrt(sigma))
Upper = Upper_Mach - overspeed buffer / (a sqrt(sigma))
q = 0.5 rho TAS^2  =  0.5 gamma p M^2     (equal when the same T_static is
                                            used for rho and for a; SI units)
1 psf = 47.88025898 Pa
Stall — Vs_ref·√(W/W_ref) then the selected degradation convention:
A aerodynamic (explicit CLmax loss), B legacy linear ice heuristic,
C ice mapped to CLmax. Never apply two at once. C is algebraically identical to
B — 1/√(1−(1−1/(1+x)²)) = 1+x — and the tool says so wherever C appears.
Speed-band indicator — an equivalent-airspeed axis in knots, with the amber row
beneath it expressing the same axis as Mach at the current altitude and temperature.
The dashed amber rectangle is the raw aerodynamic interval, from modelled stall to
operating ceiling, with no buffers applied; the solid green span is the user buffer
interval, inside both of your buffers, so at least the stall buffer above the stall and
the overspeed buffer below the ceiling 
v2.6 r1 - Storm...7 (1).html
. On screen the spans are labelled outside the
raw aerodynamic interval, caution - inside the raw interval, short of a buffer and
buffered - inside the user buffer interval, alongside a △ marker for the current
Mach-derived EAS 
v2.6 r1 - Storm...7 (1).html
. The words safe and danger are deliberately not used.
CLmax sensitivity — a pure aerodynamic sweep of the selected stall reference. It is
applied to the reference, which may itself already carry a CLmax loss (the 185
chart-derived reference does). The envelope's ice and CLmax convention is not applied
to that table, so its margin column will not match the headline margin whenever an ice
convention or a CLmax-loss input is active. It does not infer CLmax loss from ice
thickness, cloud reflectivity, temperature or radio reports 
v2.6 r1 - Storm...7 (1).html
.
Ice scenario table — a linear legacy heuristic, and it says so: Convention B sweep —
computed with the linear rule regardless of the convention selected above, so these rows
are not the model in force; the headline modelled stall uses the selected convention.
The row where the margin reaches zero is always included, and the row matching the
entered ice percentage is highlighted.
Dynamic pressure — computed in SI units throughout.
What the DIVE tab will and will not do
The tab reconstructs the ground-referenced trajectory first and produces air-relative
estimates only when track, wind, vertical-wind, pressure-altitude and temperature
information are supplied. Its own guardrails, stated on the page:

Wind correction requires a true track and a wind direction reported as wind FROM.
Vertical wind is subtracted from ground vertical speed to estimate air-relative
vertical motion.
Mach uses local speed of sound from the supplied static temperature; q also requires
pressure altitude.
No impact speed, impact-G or elevator-failure estimate is produced from sparse points.
Groundspeed is not true airspeed, and sparse ADS-B data cannot establish aircraft control
state or accident cause.

Evidence the dive reconstruction still needs 
v2.6 r1 - Storm...7 (1).html
:

Aircraft-specific AFM / approved stall-speed data and flap schedule.
Actual aircraft weight, CG and configuration at the relevant time.
FDR: Mach, calibrated/indicated airspeed, AoA, pitch, roll, control positions, trim,
vertical acceleration, AP modes and disconnect.
CVR and ATC audio with verified timestamps.
Pressure altitude, GPS altitude, SAT/TAT, wind vector and radar/sounding data.
Wreckage examination, elevator fracture analysis and maintenance history.
Operator training and simulator-session records.
The storm-distance study tool
Distance to reference point, groundspeed, and two user-set study buffers — an
ordinary-cell buffer and a severe-cell buffer. The tool's own warning 
v2.6 r1 - Storm...7 (1).html
:

The buffers are user-defined study values, not universal regulatory minima. Confirm
current local guidance and consider storm movement, growth, route geometry and
manoeuvring space. Times are distance divided by groundspeed; they are not reaction-time
guarantees or declarations of safe separation.

Recovery material — classification only
The tool carries a table of flight regimes and why each must stay separate: high-speed
spiral/dive, conventional wing stall, deep/super stall, tailplane stall, flat spin, and
control-surface failure. It is labelled Recovery material - classification only 
v2.6 r1 - Storm...7 (1).html
,
and it is not a checklist or flight instruction: no control inputs are offered anywhere
in the tool. Use the applicable AFM/QRH and approved upset-recovery training.

The case tab — hypothesis and teaching material
The tab opens with its own statement, which is also the limit on everything it contains:

CASE STATUS: HYPOTHESIS / TEACHING MATERIAL. The following is a structured restatement
of the supplied v2.0/v2.2 calculator and discussion. It is not an NTSB probable-cause
finding and has not been independently verified in this file. No victims, crew or family
members are named.

Each row of the N722BD timeline carries its own evidence status — REPORTED, MODELLED,
MIXED or MEASURED — and the reported entries are marked REPORTED - VERIFY. Competing
mechanisms are listed without being ranked as findings, and the tab ends with the list of
evidence still needed 
v2.6 r1 - Storm...7 (1).html
.

Data provenance — read before trusting a number
143.3 KEAS (discussion model) — a discussion-derived KIAS figure treated as a KEAS
proxy, with no IAS/CAS installation correction applied. Not a certified value.
185.0 kt (chart model) — back-calculated from a commentary chart stall line.
185.00 = 143.3 × 1/√(1 − 0.40) exactly, so it already carries about 40 % CLmax loss.
VMO 340 · MMO 0.81 general · stepped M0.78 at and above FL370 — published figures.
The tool states the position plainly: Three MMO figures circulate publicly: 0.78 / 0.80
/ 0.81. Only the applicable AFM settles the approved value. This model can compare
them; it cannot establish which is approved for a particular aircraft 
v2.6 r1 - Storm...7 (1).html
. The stepped
limit can be set to apply at or above the stepped altitude, strictly above it, or
not at all 
v2.6 r1 - Storm...7 (1).html
.
Evidence tier (selected configuration) — every configuration carries one of
CERTIFIED, TYPE-DATA, MEASURED, REPORTED, EXPERIMENTAL, MODELLED, ILLUSTRATIVE or
UNKNOWN, together with a source / aircraft-document reference 
v2.6 r1 - Storm...7 (1).html
.
User-defined study margins — Analytical buffers selected by the user. Not approved
operating margins and not regulatory limits 
v2.6 r1 - Storm...7 (1).html
.
Case presets — Presets load the scenario conditions together with the stated stall
reference and degradation convention, so each published figure stays reproducible 
v2.6 r1 - Storm...7 (1).html
.
Replace the presets with your own AFM/POH figures and set the tier to match the
document you used.

Limits, stated plainly
The CASE STUDY tab is a structured restatement of supplied discussion material —
hypothesis and teaching material, not an NTSB probable-cause finding, and not
independently verified in this file. No victims, crew or family members are named.
Sparse ADS-B data cannot establish aircraft control state or accident cause.
Groundspeed is not true airspeed. No impact speed, impact-G or elevator-failure estimate
is produced from sparse points.
The recovery material is classification only — no control inputs are offered
anywhere in the tool.
The band indicator and the verdict are study aids. They carry no regulatory authority
and are not operating clearances.
The tool stores nothing: every configuration, source string and dive point is discarded
when the tab closes.
Release history
Every build, every defect, every digest — including the two defects the suite found in
its own new code.

BUILD
CHECKS
STATUS
v2.1
—
root correction: the m/s→kt factor was wrong, scaling the sound speed by 15 %
v2.2
48
piston mode, ADS-B dive reconstruction, eight-tier evidence table
v2.3
55
✅ browser-verified 2026-11-08 · the mandatory +1 in the CAS relation
v2.4
67
✅ browser-verified 2026-11-10 · stall-TAS display defect found in the same run
v2.5
70
√σ stall-TAS fix + three DOM-reading regression guards
v2.6
83
✗ browser-tested 82/83 — its own new guard found a defect in the new status code
v2.6 r1
83
✅ RELEASED — browser-verified 2026-11-10, checksummed


v2.1 — the root correction
The metres-per-second → knots and → mph factors were wrong; they were not conversions at
all. The sound speed was scaled by 15 %, and every Mach-derived number with it. Corrected:
sound speed at FL350 is 576.4 kt (663.4 mph), not 500.5 kt, and a·√σ at FL350 is
320.9 kt, not 278.9 kt.

The earlier "0.87 kt policy window" claim for the N722BD top of climb was an artefact of
that error. The true figures are a 34.8 kt policy window, a +38.9 kt stall margin
at +10 % ice, and a margin that does not reach zero until 31 % ice accretion. The
band for this airframe closes near FL433, not FL415.

Also in v2.1: generic IAS labels replaced with EAS; explicit KCAS handling for VMO; CLmax
degradation separated from ice coverage; per-configuration stall data made editable;
blank-input handling corrected and required inputs made to fail visibly; policy-window
closure reworked to include both the stall and the overspeed buffer; the dive logic
corrected (groundspeed + vertical speed is ground-relative, not TAS; GPS altitude separated
from pressure altitude; sparse-data impact speed and G-force extrapolation removed;
recovery commands replaced by non-operational regime classifications).

v2.2 — features
Piston mode (IAS stall margin, piston icing hazards). The DIVE pressure-altitude
cross-check, which exposes the frozen pressure-altitude field in the N722BD final report.
Eight-tier evidence table. Per-configuration stall data with evidence tier and source
reference. User-defined storm buffers. Wind-aware dive reconstruction. Checks: 48.

v2.3 — three real corrections
The mandatory +1. The supplied v2.2 printed M_CAS = √(5[(qc/p₀)^(2/7) − 1]). The
correct relation is M_CAS = √(5[(1 + qc/p₀)^(2/7) − 1]). As printed, the bracket is
negative for every realistic calibrated airspeed, so the expression returned NaN. The
corrected form is pinned by a round-trip test plus a check that the old form is not
finite.
One degradation convention. The stall degradation had been ambiguous — a base
speed already carrying a CLmax loss, multiplied again by an ice percentage, against a
separate CLmax-loss input. Three mutually exclusive conventions were introduced: A
aerodynamic, B legacy ice heuristic, C ice mapped to CLmax, with the equivalence
stated: 143.3 × 1/√(1 − 0.40) = 185.00 exactly, and +10 % ice on the 185 reference
equals a 17.36 % CLmax loss — 50.41 % in total against the 143.3 clean reference.
Strict airspeed labels. EAS, KEAS, KCAS and KIAS used separately and consistently.
The proxy treatment of a KIAS-derived figure as a KEAS input is disclosed where it
applies.
Also: the hard-coded storm minimum removed; recovery material reduced to classification
only; the tropopause pressure taken continuously from the troposphere formula; dynamic
pressure corrected from a knots-based to an SI computation; the EAS identity check
corrected (it had compared a knots value against an SI identity, so it could never pass).

Checks: 55. Browser-verified 2026-11-08 — 55/55. Known-good fallback.

v2.4 — restore and disclose
The speed-band indicator and the editable per-configuration stall table — both dropped by
the v2.3 rebuild — were restored. The Copy brief action was added. The CLmax-table
wording was corrected (it had said "clean reference" when the reference may already carry
a CLmax loss).

Checks: 67. Browser-verified 2026-11-10 — 67/67. The same run exposed a defect:

The "Stall (modelled)" TAS cell divided EAS by σ instead of √σ — a factor of 1.837.
It printed 686.9 kt where the physics gives 373.9 kt: faster than the 474.7 kt
ceiling TAS on the same page, at a lower Mach, at the same altitude where the speed of
sound is a single number. Impossible, and visible on the page. One display cell; no
physics depended on it. Present in v2.3 and v2.4.

Retained as the known-good v2.4 fallback, with the defect documented.

v2.5 — the √σ fix and the guards that would have caught it
The stall-TAS cell corrected to EAS/√σ. The CLmax-table columns relabelled ("Current
margin" → "Margin at this CLmax loss"; "User-buffer interval" → "Buffer interval at this
loss"), because the margin column of that sweep is not comparable with the headline
margin when an ice convention is active. The two brown caution zones named explicitly. The
relation TAS = EAS/√σ stated in the equations panel.

Three regression guards were added — and the important part is how they are written.
They read the rendered DOM, not the formulas, because a formula-level assertion cannot
see a display defect:

the rendered stall TAS cell equals stall EAS/√σ — an exact string comparison;
the rendered stall TAS agrees with the rendered stall Mach and the local speed of sound,
TAS = M·a — state-independent, and it catches dividing by σ, by σ², multiplying, or
transposing columns;
when the current EAS is above the modelled stall, the stall point must be a slower
condition than the present state.
Checks: 70. Not executed in a browser at the time — which is why the defect was caught
in the next build's run rather than here.

v2.6 — the deployment review
Visible wording brought inside the tool's own evidence discipline. SAFE →
BUFFERED. DANGER → OUTSIDE BAND. ABOVE THE OPERATING LIMIT → ABOVE THE MODELLED CEILING. NO COMPLIANT SPEED → NO USABLE SPEED BAND. The verdict colour class go
renamed ok, so the token GO appears nowhere in the source.

One status stamp became two. The build stamp reports the software only. A second
input-state stamp reports validation errors, advisory notes and the evidence tier, and is
never rendered in the green state. The green build stamp therefore cannot appear
alongside a failed or warning state.

The suite was pinned to a fixture (JET, FL35250, ISA, convention A, +10 % ice, M0.76,
27 500 lb, 10/10 buffers) and restores the user's inputs afterwards, so the stamp no longer
turns red when the user changes inputs or switches to PISTON mode.

Two false greens closed. An EAS above the user's buffered ceiling — inside the raw
aerodynamic interval, in the tool's own brown caution zone — was being reported as "WITHIN
THE USER BUFFER" in green; it is now reported as caution. And a hard validation failure
could no longer leave a positive verdict on screen.

Also: convention C disclosed as algebraically identical to convention B, with a guard
pinning the identity; esc() taught to escape quotes; the exported brief made to state
the computed ISA temperature instead of a fixed string; the ice table taught to highlight
the entered ice percentage and to state that it is not the model in force; and the tool
made to open on the published N722BD case so the ENVELOPE and CASE tabs agree.

Checks: 83. Browser-tested 2026-11-10 — 82/83. The failing check was the tool's own:


Collapse
Save
Copy
1
DEPLOYMENT: a validation error forces the build stamp out of its green state
Cause. updateStatus() evaluated the suite-failed branch before the input-state
branch, and during the first run STAMP_SUITE.ok was still false — the suite result is
recorded only after the checks have executed. The stamp therefore read
SELF-TEST FAILED while the checks were still running, and the validation-error text
never reached it.

Why this is the good outcome. A build that had reported 83/83 on its first run would
have been the suspicious one: it would have meant the new guards could not fail. The 83rd
check found a genuine ordering defect in code written that same morning. The suite
earned its place in the first hour by refusing to let the work through unchecked.

v2.6 r1 — the release
The stamp fix. STAMP_SUITE gained a running flag, so the stamp reads
SELF-TEST RUNNING while the suite executes instead of falsely claiming failure. The
input-state branch was promoted above the suite branch, so a validation error is always
reported. The check itself was corrected — it had looked for the validation-error text in
the build stamp, when by design that text belongs to the input-state stamp; it now
asserts that the build stamp is out of the green state and that the input-state stamp
is red and carries the validation error.

Also: the hard-coded "about 40 percent loss" clause removed from the convention-B note
(true only for the 185 reference); the redundant SELF-TEST FAILED suffix replaced with
SUITE FAILED - SEE REFERENCE & TESTS; version strings set to v2.6 r1.

No physics changed between v2.6 and v2.6 r1. Every number on the page is identical
between the two runs.

Checks: 83. Browser-verified 2026-11-10 — 83/83, cold first load.

Released. SHA-256 1e9771a4b40309c2b578156025052d582eca7b0f60d00a33f6925ed4e79e89e8,
110 211 bytes, CRLF.

Digests
BUILD
BYTES
SHA-256
v2.5
98 777
c9a9dcc6b6027672318b386d5d81c9a57d6c103f8699e4343383a386d94a8975
v2.6
108 498
6784a4cb8864c0521ac15d690b316faeeaa500bff62d9b17c318f2b2f510488c
v2.6 r1
110 211
**1e9771a4b40309c2b578156025052d582eca7b0f60d00a33f6925ed4e79e89e8


The store copies use LF and the released artefacts use CRLF, which is why the sizes differ
by exactly one byte per line. verify_release.ps1 normalises before hashing, so either
form validates. The digest identifies the bytes that were released.

Standing weaknesses, recorded not fixed
Five checks are self-referential — wind correction, vertical wind, derived vertical
rate, PA-staleness threshold, and the no-GO/NO-GO source scan. They certify
documentation, not behaviour, and cannot fail if the formula drifts.
The CLmax guard is a warning, not a hard stop. The stall factor clamps loss to
0.9999, so a bypassed warning would yield a 10× stall speed rather than a refusal.
PISTON mode reuses the Mach field as IAS, and the field keeps its value across a
mode switch — a stale IAS can be carried silently.
No persistence. Configurations, tiers, source strings and dive points are lost on
reload. A localStorage save plus JSON export/import is the highest-value addition.
The dive "3D TAS" resolves the along-track wind only; a crosswind is not resolved.
Case-tab rows marked MEASURED carry no source citation. An NTSB report number and
date on those rows would make the evidence discipline internally consistent.
The track's knot scale stops at 250 while the axis runs to 284 — the right-hand
12 %, including the whole outside-the-band zone, has no scale reference beneath it.
The ice table labels negative-margin rows "MARGIN REACHED ZERO" — true, but
imprecise next to the single zero-crossing row.
Repository layout

Collapse

Run
Save
Copy
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
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
Rebuilding from source. make_v2_6_release.ps1 applies 31 asserted literal
replacements to the v2.5 base; patch_v2_6_r1.ps1 applies 12 more. Both abort without
writing if any anchor fails to match exactly once, so the chain is derived rather than
transcribed. verify_v2_6_release.ps1 is the independent gate — it does not trust the
builder.

Licence
MIT for the code, with an explicit carve-out on the aviation content — see LICENSE.

Credits
Built by Sierra 7 (S7-TWK) with Zulu 7. Offline single-file study application;
no external libraries, no tracking, no network calls.

A number on a screen is a claim about the world. It has to be checked by something other
than the formula that produced it.


v2.6 r1 - Storm...7 (1).html
 Coffin Corner Calculator v2.6 r1 — release/v2.6-r1/coffin-corner-calculator-v2.6-r1.html, the released file this document describes.

