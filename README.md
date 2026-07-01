# AI Kickstart · Workshop Delivery Kit

A self-contained, git-ready kit for superluminar consultants to run an **AI Kickstart**: take the one use case a client already wants to build, pressure-test the data behind it, and hand over a build-ready plan. It ends in a written report and a recommended first engagement. A decision, not a guess.

> **What this is:** the lighter, faster companion to the **AI Readiness Workshop**. AI Kickstart is a deliberately trimmed subset of that workshop. Where AI Readiness scores the whole organisation across five dimensions and surfaces the use cases worth building, Kickstart assumes the client already knows what they want to build and scopes to one use case. We keep only the parts of the Readiness method that decide whether *this one build* can start.

---

## What AI Kickstart is (and isn't)

- **Is:** a diagnostic on one use case. Platform ready? People ready, with us alongside? Compliance burden for this use case? And the real gate: does the data hold up?
- **Isn't:** an org-wide assessment. No cross-functional readiness sweep, no portfolio of use cases. If a fuller picture is needed, that's the **AI Readiness Workshop** (see cross-sell note below).

We are not a vendor, a sparring partner. You own what we build. If the data won't support the use case, you'll hear that plainly: a clear no beats an expensive maybe. No slideware. Everything is concrete, written down, and yours to keep.

---

## What it derives from AI Readiness (the trimmed subset)

| AI Readiness Workshop | AI Kickstart (this kit) |
|---|---|
| Org-wide readiness across **5 dimensions**, scored 0–5 in depth | The **same 5 dimensions** read lightly (heuristic only), surfaced as a **high-level snapshot** of **3 status cards** (Platform / People / Compliance) for one use case |
| Surfaces and prioritises a **portfolio** of use cases | Client brings **one** use case; we pressure-test it |
| Full data assessment across candidate use cases | A focused **use-case data check**, the gate |
| Broad architecture & roadmap | One **reference architecture** + **indicative cost** + **first engagement** |

The five readiness dimensions are unchanged: **Data; Cloud & infrastructure; Governance & compliance; Skills; Organisational appetite.** Kickstart reads them lightly and folds them into the three lenses **Platform / People / Compliance**.

---

## Who runs it

Two superluminar consultants, both engineers, running it together. No fixed split: they share the room, the feasibility, and the architecture. Light governance input is pulled in as needed. See `02-facilitator-runbook.md` for who needs to be in the room on the client side.

---

## The short flow

1. **Intake.** Client completes `01-intake-questionnaire.md` as pre-work (one use case, the data behind it, the AWS estate).
2. **Pressure-test session.** Short, facilitated, mapped to the three workshop steps:
   1. **Bring the use case** (capture it; quick readiness read)
   2. **Pressure-test it** (data check + feasibility)
   3. **Hand you the build plan** (architecture, cost, first engagement)
3. **Build plan.** Consultant drafts the one architecture pattern, sizes the effort and run cost, and shapes the recommended first engagement (Phase 0 first).
4. **Report.** The 5 deliverables, assembled per `04-report-outline.md`, plus the executive summary and the editable draw.io diagram source.

The session itself is a short depth-gathering session on the one use case and the data behind it. The plan and report are built off-line on a fast (~1 week) turnaround. See the runbook's "Engagement shape (fast turnaround)" section in `02-facilitator-runbook.md`.

---

## File index

| File | Purpose |
|---|---|
| `README.md` | This file: what the kit is, how it maps to the report, how to run it. |
| `01-intake-questionnaire.md` | Client pre-work: one use case, its data, the AWS estate, light readiness inputs. |
| `02-facilitator-runbook.md` | Agenda, timings, roster, facilitation notes, pre/post checklists, pitfalls. |
| `03-facilitator-field-guide.md` | The single in-room reference to judge *against*, in workshop order: readiness snapshot (the three lenses), use-case canvas, data-check gate, cost basis, reference architecture patterns. Holds the definitions, anchors and worked examples; live capture goes in the Notion workbook. |
| `04-report-outline.md` | The 5-deliverable report structure + executive summary + generator field map. |

Kickstart has no facilitator deck.

---

## Mapping: kit files → the 5 report deliverables

| Report deliverable | Built from |
|---|---|
| **D1 · Readiness snapshot** (3 status cards: Platform / People / Compliance) | `03-facilitator-field-guide.md` (section 1 · Readiness snapshot), read against `01-intake-questionnaire.md` |
| **D2 · Use-case data check** (the gate) | `03-facilitator-field-guide.md` (section 3 · Data-check gate), fed by section 2 · Use-case canvas |
| **D3 · Reference architecture** | `03-facilitator-field-guide.md` (section 5 · Reference architecture) |
| **D4 · Indicative cost estimate** | `03-facilitator-field-guide.md` (section 4 · Cost basis) |
| **D5 · Recommended first engagement** | synthesised from D2–D4, structured in `04-report-outline.md` |

The executive summary and the report assembly itself live in `04-report-outline.md`.

---

## Cross-sell note → AI Readiness Workshop

Kickstart answers "can we build *this one thing*?" If during the session the client realises they need the fuller picture, readiness across the organisation and the *other* use cases worth building, prioritised, that is exactly what the **AI Readiness Workshop** is for. Flag it in the D1 verdict (see the example: *"If you want a fuller picture of your readiness across the organisation, and the other use cases worth building, that is what our AI Readiness Workshop is for."*). It's a natural next step, not an upsell.

---

## Economics

The kit sizes delivery effort (person-days) and estimates the AWS run cost (AWS's pricing, from the Pricing Calculator, not a number we set). It does not set a day rate or a price: those are owned by sales and compiled with them when the report is built. Engagements are phased, Phase 0 first. Any euro figure in the kit comes from the published example report and is an illustration, not a quote.

---

## Report generator

The report is produced by superluminar's report generator, live at `https://a2hmr6fzsm.eu-central-1.awsapprunner.com/` (route `/new/kickstart`; access password is in the shared 1Password). It also runs locally on `:8000` for development. Fill the form from `04-report-outline.md`, which ends with the field spec the generator is built to.

## Conventions

- **European data realities are first-class:** GDPR, EU AI Act classification, data residency, **eu-central-1 (Frankfurt)**.
- **AWS-native, managed by default:** Amazon Bedrock (+ Knowledge Bases, Guardrails), Amazon Textract, Step Functions, Lambda, S3, DynamoDB, CloudWatch, IAM; S3 Vectors vs OpenSearch Serverless for retrieval.
- **Capability transfer:** we embed, build alongside the client's team, and hand over.
- **British/European spelling** throughout (prioritised, organisational).
- Cross-references are **relative filenames within this folder**. The kit is self-contained and git-ready.
