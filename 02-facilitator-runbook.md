# 02 · Facilitator Runbook

**AI Kickstart · superluminar GmbH**

This is the light, fast engagement. One use case, one session (plus prep and write-up). Your job is to get the client from "we want to build X" to "here's the build-ready plan, and here's the one thing that decides it." End on a written report and a recommended first engagement. A decision, not a guess.

> AI Kickstart is a trimmed subset of the AI Readiness Workshop. Don't run an org-wide assessment. Stay on the three lenses (Platform / People / Compliance) and the data check. If the client clearly needs the fuller picture, name the **AI Readiness Workshop** and move on. Don't drift into it.

**Voice in the room:** honest, plain-spoken, direct. *Not a vendor, a sparring partner. You own what we build.* If the data won't support it, say so plainly: *a clear no beats an expensive maybe.*

---

## The three steps (everything maps to these)

1. **Bring the use case.** Capture it cleanly; take a quick readiness read for context.
2. **Pressure-test it.** Data check + feasibility. The gate lives here.
3. **Hand you the build plan.** Reference architecture, indicative cost, recommended first engagement.

---

## Engagement shape (fast turnaround)

Like the bigger workshops, the session gathers depth and the plan is finished off-line. The difference is scale: one use case, five deliverables, one architecture pattern, so there is far less to finish. Keep the whole thing to about a week elapsed, not a multi-week engagement.

| Phase | Who | Indicative |
|---|---|---|
| 1 · Intake & prep | superluminar | Read the intake, confirm the one use case and its pattern, flag any obvious blocker. ~half a day. |
| 2 · The session | the two consultants + the room | One focused ~3-hour session, or two short remote blocks. Gather depth on the use case and the data behind it. |
| 3 · Off-line synthesis & report | superluminar | Finalise the data-check verdicts, draw the one architecture, size effort, estimate the AWS run cost, write the 5-deliverable report. ~1 to 2 days. |
| 4 · Readout | a consultant + use-case owner | Walk the plan and the decision. ~1 hour. |

If the use case opens up into something broader, that is the signal for the **AI Readiness Workshop**, not a longer Kickstart.

---

## Who's in the room (client side)

| Role | Why they're needed | Step |
|---|---|---|
| **Use-case owner** | Owns the problem and the "good enough to ship" bar. Decision-maker. | 1, 3 |
| **Data owner** | Knows where the data lives, its quality, and whether a labelled set exists. | 2 |
| **Engineer / platform contact** | Knows the AWS estate and the target system's integration reality. | 2, 3 |
| **Light governance input** | GDPR / AI Act / residency questions for *this* use case. Can be on-call rather than full-time. | 2 |

superluminar side: **two consultants** (both engineers), running it together. No fixed split, they share the room, the feasibility, and the architecture.

---

## Timing: one focused session (~3 hours)

Adjust to taste; this is the fast one. Half-day on-site or two shorter remote blocks both work. The session's job is to gather depth on the one use case and the data behind it, not to produce the deliverables: complete the canvas and the data check from evidence, push for the number and the example, and leave the costing and the report for off-line. The intake (`01`) captures the basics ahead of time so the room goes straight to the data.

| Time | Block | Step | Outcome |
|---|---|---|---|
| 0:00–0:15 | **Frame it.** What Kickstart is, what it isn't, how the session ends. Set the "honest no" expectation. | n/a | Shared expectations |
| 0:15–0:45 | **Bring the use case.** Walk the intake; complete the use-case canvas live (capture in the Notion workbook; judge against `03-facilitator-field-guide.md`, section 2 · Use-case canvas). | 1 | Canvas filled |
| 0:45–1:05 | **Quick readiness read.** Score the 3 lenses lightly against `03-facilitator-field-guide.md` (section 1 · Readiness snapshot). | 1 | Draft D1 |
| 1:05–1:15 | Break | n/a | |
| 1:15–2:15 | **Pressure-test the data.** Work the data check row by row against `03-facilitator-field-guide.md` (section 3 · Data-check gate). This is the gate. | 2 | Draft D2 |
| 2:15–2:45 | **Feasibility & architecture.** Design the architecture (see `03-facilitator-field-guide.md`, section 5 · Reference architecture); sketch it; mark the human-in-the-loop and integration points. | 2→3 | Draft D3 |
| 2:45–3:00 | **The first step + the measure.** Outline Phase 0 / Phase 1, rough effort & run cost, scope/out-of-scope. Capture the expected benefit and the 1–2 KPIs the phase gates will measure (see below). | 3 | Draft D4, D5 |

Cost detail and the polished report are completed after the session, not live.

---

## What to capture (so the report writes itself)

Capture against the field map in `04-report-outline.md`. Minimum:

- [ ] One-sentence use case + the assist/decide call
- [ ] The canvas (problem, process, who feels it, value, "good enough to ship", integration points)
- [ ] The 3-lens snapshot with a one-line justification each
- [ ] **The go/no-go read:** Proceed / Proceed with caution / Pause, with any blocker named (see below)
- [ ] The data-check rows with **State** (Usable / Partial / Messy / Blocker) and "what to do"
- [ ] **What actually decides this:** the 1–2 real gates (often *labelled set* + *integration*)
- [ ] The honest "if accuracy falls short on messier cases" call
- [ ] Chosen architecture pattern + where the human-in-the-loop sits + EU residency note
- [ ] Phase 0 vs Phase 1 split (person-days), monthly run line items, the cost driver
- [ ] **The expected benefit (plain terms, order of magnitude) and the 1–2 KPIs the phase gates measure** (see below)
- [ ] Recommended first engagement: scope, out-of-scope, what you get, the decision

---

## The go/no-go read (light)

The three-lens snapshot and the data check each carry their own honest read. This is the **one-line synthesis** that sits on top of them, so the client gets a single verdict before the detail: should we build this, and is anything in the way. It does **not** repeat the snapshot or re-score anything; it reads the snapshot statuses and the data-check States together and lands on one of three:

- **Proceed.** Snapshot is `Ready` / `Ready, with us alongside` / `Low burden` across the board, and no data row is a Blocker that stops the build. The usual Kickstart outcome. It sits quietly in the verdict.
- **Proceed with caution.** Buildable, but a Blocker or a `Partial` becomes named Phase 0 work that has to land first (typically the labelled set or the integration). Most "worth building, once two gaps are closed" cases live here.
- **Pause.** A `Gap` on a lens, or a Blocker with no Phase 0 path, stops the build until it is resolved (a high-risk AI-Act classification, no platform path, no one to own it). Say so plainly and early.

Name the blocker if there is one. For most clients this is **Proceed**; when it is Caution or Pause, it leads the readout, because saying so early is the honest thing. *A clear no beats an expensive maybe.*

> *Worked example (Brückner):* **Proceed with caution.** "Worth building. Two gaps, the labelled set and the ERP write path, are named as Phase 0 and close before the build goes live."

---

## Value & success metrics (KPIs), light

One use case, so this is small: a sentence on the **expected benefit** and **one or two KPIs**, no more. The point is that the build's value is **measured, not promised**: the same KPIs are what the phase gates check, so the engagement only widens when the numbers clear the bar. Keep it honest and bounded; we do not manufacture an ROI figure (no NPV, no payback model, that is the client's business case to own).

Capture, for the recommended build:

- **Expected benefit.** What changes if it works, in plain language, with a rough order of magnitude (a share of the work posted straight through, hours off the manual task, errors avoided). Not a spreadsheet.
- **1 to 2 KPIs.** Each is a **metric, a baseline, a target, and when it is measured**. The baseline is the number today (often effectively zero, or "no eval set yet", which is itself a finding). The target is the bar that says "this earned its place". The "when measured" ties the KPI to a phase gate.

> A use case whose value you cannot state and cannot measure is not ready to recommend. Defining the metric up front is how you protect the client from spending the budget and never knowing whether it worked.

### Worked example · Brückner (invoice extraction)

- **Expected benefit.** Take the daily re-keying of supplier invoices off the AP team and post the clean, high-confidence ones straight through, with people handling only the uncertain cases. Order of magnitude: a measured share posted without a person, not "replace AP".

| KPI | Baseline (today) | Target | Measured |
|---|---|---|---|
| Straight-through posting rate | ~0% (every invoice keyed by hand) | a measured, agreed share posted without a person | Phase 1 rollout, on a real stream |
| Accuracy on the messier suppliers | none (no labelled set yet) | clears the agreed accuracy bar on the labelled set | Phase 0 gate, on the labelled set |

The labelled-set gate tests the second KPI before any extraction goes live; the rollout tests the first. If accuracy does not clear its bar on the messier suppliers, that is the signal to keep them on human review and automate the clean ones first, not to widen. *A clear no beats an expensive maybe.*

---

## Facilitation notes

- **Keep it to one use case.** If a second appears, park it on a "for AI Readiness" list and carry on.
- **Spend your time on the data, not the model.** For most patterns the model can do the task; what decides it is the *labelled set* to prove accuracy and a *clean integration* to land results. Steer the room there.
- **Make the gate explicit.** Each data row gets a State. A single **Blocker** doesn't kill the build; it usually becomes Phase 0 work. Name it as such.
- **Surface the honest call early.** If messier cases will likely fall short, say so now and frame the human-review fallback. Don't save bad news for the report.
- **Managed by default.** Reach for managed AWS services; only add bespoke pieces where the use case genuinely needs them.
- **Hand over as you go.** Frame every recommendation as something their team will own. *You own what we build.*

---

## Pitfalls

- **Scope creep into an org assessment.** That's a different workshop. Hold the line.
- **Letting "the AI can do it" stand in for "it'll ship."** The data check, not the demo, decides shipping.
- **No labelled set, glossed over.** This is the most common real gate. Don't let it slide; it's Phase 0.
- **Integration assumed, not checked.** "We'll just write it back to the ERP" is exactly where Blockers hide. Get the client's engineer to confirm there's a real, permissioned write path.
- **Over-precise costs.** Everything is an illustrative ballpark. Say so, and state your assumptions.
- **Promising full automation.** Human review for low-confidence cases stays. That's a feature, not a failure.

---

## Pre-session checklist (facilitator)

- [ ] Intake (`01-intake-questionnaire.md`) received and read
- [ ] Confirmed the **one** use case and its pattern
- [ ] Right people confirmed in the room (use-case owner, data owner, engineer, governance on-call)
- [ ] Client's row in the **AI Kickstart Engagements** Notion workbook open for live capture (canvas, snapshot, data check, cost all live there now)
- [ ] Field guide (`03-facilitator-field-guide.md`) at hand to judge *against*, not to write into: readiness snapshot (section 1), use-case canvas (section 2), data-check gate (section 3), cost basis (section 4), architecture patterns (section 5). The relevant architecture pattern pre-selected; the rate and price come from sales, not the kit
- [ ] Flagged any obvious Blocker or compliance concern to raise early

## Post-session checklist (facilitator)

- [ ] All 5 deliverables drafted (D1–D5)
- [ ] Data-check States agreed with the data owner
- [ ] Architecture diagram drawn; **editable draw.io source** prepared to ship alongside
- [ ] Cost estimate completed with assumptions stated; Phase 0/Phase 1 split clear
- [ ] Recommended first engagement: scope, out-of-scope, what-you-get, the decision
- [ ] Go/no-go read landed (Proceed / Proceed with caution / Pause) with any blocker named
- [ ] Expected benefit + the 1–2 KPIs captured, each tied to the phase gate that measures it
- [ ] Executive summary written ("the short version" / why it fits / what stands in the way / what to do first + hero stat boxes)
- [ ] Cross-sell to AI Readiness included in D1 verdict (if relevant)
- [ ] Report reviewed against `04-report-outline.md` and sent
