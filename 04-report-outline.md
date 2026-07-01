# 04 · Report Outline

**AI Kickstart · superluminar GmbH**

How the deliverable report is assembled. Cover, executive summary, then the **five deliverables** in order. Concrete, written down, yours to keep. **No slideware.** Every figure is an **illustrative ballpark, not a quote.**

---

## Cover

- Title: **AI Kickstart**, "One use case, checked and costed."
- Strap: *You already know what you want to build. We take that one use case, check the data behind it, and hand you a build-ready plan: architecture, costs, and a clear first step.*
- **Prepared for:** [client name], [industry · size · location · platform status].
- **Prepared by:** superluminar · AWS Advanced Consulting Partner.
- (For samples, mark **EXAMPLE / illustrative deliverable / fictional client** on every page.)

---

## Executive summary

Four short blocks plus three hero stat boxes. Lead with the verdict, keep it plain.

**Structure (the four blocks):**

1. **The short version.** What they came to build, whether it fits, and where the *real* work is (usually not the model; it's the labelled set and the integration). One honest paragraph.
2. **Why it fits.** The technology is proven; the platform is ready; the data/volume exists. Briefly.
3. **What stands in the way.** The 1–2 real gaps (and that neither is the model). Note Phase 0 handles them.
4. **What to do first.** The concrete first step: one document type / scope, on a real stream, with the human-in-the-loop, the rough effort, one-off cost, and run cost.

Plus **the honest part**, one line: if the data shows it won't clear the bar on the messier cases, they'll hear it before committing to full rollout. *A clear no beats an expensive maybe.*

**Three hero stat boxes:**

| Box | Content | Brückner example |
|---|---|---|
| **Verdict on the use case** | Short verdict + qualifier | *Worth building:* "Ready, once two gaps are closed" |
| **The build** | What we'd build, the stack in a phrase | *Invoice extraction:* "Textract + Bedrock, human review for low confidence" |
| **Indicative first engagement** | Price · effort · timeline · run | *~€20,000:* "14 person-days · ~5 weeks · ~€800/mo run" |

Footer line on the figures: *"All figures here are illustrative ballparks for an example client and are not a quote. They show the shape and order of magnitude of a real engagement."*

### Worked example · Brückner Hausgeräte GmbH (invoice extraction)

*Illustrative, fictional client: Stuttgart home-appliance maker, ~850 employees, already on AWS. Reproduced from the published example report to show the depth and register; not a quote.*

**1. The short version.**
> You arrived wanting to automate the data entry from incoming supplier invoices and delivery notes, which your accounts-payable team keys into the ERP by hand. It is a good fit: the technology is well understood, your AWS platform is ready, and the documents already exist. The work is not the extraction itself. It is getting a labelled set to measure against, and a clean way to post results back into the ERP. Both are doable, and this plan shows how.

**2. Why it fits.**
> Pulling structured fields from invoices is one of the most proven uses of AI on AWS. You run on AWS in eu-central-1 (Frankfurt), so a compliant build sits on what you already have. The AP team is keen to stop rekeying, and the documents arrive in volume every day.

**3. What stands in the way.**
> Two things, and neither is the model. First, there is no labelled set yet to measure accuracy against, though your ERP already holds the correct values to build one. Second, posting clean data back into the ERP needs a proper integration, not a manual paste. Phase 0 of the build handles both.

**4. What to do first.**
> Start with one document type, supplier invoices, on a real stream. High-confidence extractions post straight through; anything uncertain goes to a person to check. That is roughly 14 person-days, an indicative one-off (priced with sales), and around €800/month to run at modest volume.

**The honest part.**
> If the labelled set shows accuracy is not good enough on your messier suppliers, you will hear that before you commit to a full rollout. The MVP exists to prove it on your own invoices.

**Three hero stat boxes (Brückner):**

| Box | Value | Qualifier line |
|---|---|---|
| **Verdict on the use case** | Worth building | Ready, once two gaps are closed |
| **The build** | Invoice extraction | Textract + Bedrock, human review for low confidence |
| **Indicative first engagement** | priced with sales | 14 person-days · ~5 weeks · ~€800/mo run |

> The published example PDF shows the one-off as ~€20,000. That euro figure is the published illustration only; in a real engagement the price is compiled with sales at their rate against the 14 person-days. The kit asserts effort and run cost, not a price.

---

## Deliverable 01 · AI readiness snapshot

*Source: `03-facilitator-field-guide.md` (section 1 · Readiness snapshot).*

- Frame: a **high-level** read on whether the ground is ready for *this* build, not an org-wide assessment. Just **the three lenses**.
- Three readiness cards, each = a **status label** + the **area** (lens) + one/two honest lines. The status is a **label, not a 0–5 score.** Allowed status values: `Ready` / `Ready, with us alongside` / `Low burden` / `Partial` / `Gap`.
  - **Platform:** is the ground ready?
  - **People:** ready, with us alongside?
  - **Compliance:** burden for this use case?
- **Verdict callout** (heading + body), e.g. "Ready to build. The one real dependency is the data behind it, which the next page checks in detail."
- **Cross-sell** (if relevant): point to the **AI Readiness Workshop** for the fuller, organisation-wide picture and the other use cases worth building.

---

## Deliverable 02 · Use-case data check (the gate)

*Source: `03-facilitator-field-guide.md` (section 3 · Data-check gate).*

- Frame: **this is the gate.** The extraction/build itself isn't in doubt; these ~4 rows decide whether it ships.
- The **table**: `What the build needs | State | Detail, and what to do about it`, with State = **Usable / Partial / Messy / Blocker**.
- **What actually decides this:** strip to the 1–2 real gates (typically a labelled set + a clean integration) and which phase handles each.
- **The honest call:** italic line on what happens if accuracy on the messier cases falls short (keep them on human review, automate the clean ones first, you'll have the numbers).

---

## Deliverable 03 · Reference architecture

*Source: `03-facilitator-field-guide.md` (section 5 · Reference architecture).*

- The architecture as a **diagram**, designed to sit inside the client's existing **eu-central-1** account. Managed services throughout; person in the loop where the model is unsure.
- Caption noting the **editable draw.io source provided alongside**.
- **The straight-through path:** paragraph.
- **The exception path:** paragraph, including **Guardrails** (prompt-injection), **CloudWatch** logging, **IAM** least-privilege, **everything stays in the EU**.

---

## Deliverable 04 · Indicative cost estimate

*Source: `03-facilitator-field-guide.md` (section 4 · Cost basis).*

- **One-off delivery** table: effort sized in person-days, with the **Phase 0 / Phase 1** split. The euro figure is compiled with sales at their rate, not set in the kit.
- **Monthly run cost** table: line items (Textract, Bedrock tokens, Step Functions + Lambda, S3 + DynamoDB, CloudWatch) with assumptions and a total range. This is AWS's pricing, estimated from the Pricing Calculator, not a number we set.
- **Where the cost sits:** the cost driver (e.g. Textract scales with pages; digital PDFs are cheaper) and that it's sized against the real document mix.
- Rate note: the day rate is sales-owned; do not assert one in the kit. Any euro figure shown is from the published example, not a quote.

---

## Deliverable 05 · Recommended first engagement

*Source: synthesised from D2–D4; structure here.*

Laid out in full: "the decision in front of you."

- **Scope:** bulleted: the one thing built, on a live stream, with the human-in-the-loop and the Phase 0 pieces.
- **Out of scope for the MVP:** bulleted: the fast-follows, full coverage on day one, removing human review.
- **What you get:** bulleted: a working pipeline on real data, measured accuracy/straight-through rate, the labelled set + review loop to extend, the team upskilled. *You own what we build.*
- **The decision:** one paragraph: fund a [N]-day, ~€[…] MVP that proves it on the client's own data. Modest run cost, EU-resident, measured so they can widen on evidence.
- Closing hero boxes: **The build** · **Effort** · **Timeline** · **Indicative price**.
- Sign-off line: ***Not a vendor, a sparring partner.*** · superluminar · AWS Advanced Consulting Partner · Hamburg.

**Value & success metrics (the build is measured, not promised).** One short block, kept light: the **expected benefit** in plain terms (order of magnitude, no ROI model, no NPV) and **1 to 2 KPIs**, each a *metric · baseline · target · when measured*. The KPIs are not decoration: each one **is** a phase gate. The build advances only when its KPI clears the bar on the client's own data, so value is evidence, not ambition. Where a baseline does not exist yet (no labelled set), say so plainly and name the phase that establishes it. Source: `02-facilitator-runbook.md` (Value & success metrics).

> Tie the gates to the KPIs: the Phase 0 / labelled-set gate is the *accuracy* KPI clearing its bar; the rollout gate is the *straight-through* KPI clearing its bar. If a KPI misses at its gate, the client stops and rescopes rather than widening. *A clear no beats an expensive maybe.*

### Worked example · Brückner Hausgeräte GmbH (invoice extraction)

*Illustrative, fictional client. Reproduced from the published example report to show the depth and register; not a quote.*

**Scope.**
- One document type: supplier invoices, on a live stream.
- Textract for OCR, Bedrock to map to your invoice schema and validate.
- Straight-through posting for high-confidence records; human review for the rest.
- A labelled set and a measured accuracy bar, built with your team.
- A clean, permission-controlled write path into the ERP.

**Out of scope for the MVP.**
- Delivery notes and order confirmations (a fast follow once invoices work).
- Full coverage of every supplier on day one.
- Removing human review entirely. It stays for low-confidence documents.

**What you get.**
- A working pipeline running on real invoices, posting clean data to the ERP.
- A measured straight-through rate and accuracy, so you can decide on wider rollout.
- The labelled set and review loop to extend to other document types yourselves.
- Your team upskilled alongside ours. *You own what we build.*

**Value & success metrics.**
> *Expected benefit.* Take the daily re-keying of supplier invoices off your AP team and post the clean, high-confidence ones straight through, with people handling only the uncertain cases. Order of magnitude: a measured share posted without a person, not "replace AP".

| KPI | Baseline (today) | Target | Measured |
|---|---|---|---|
| Straight-through posting rate | ~0% (every invoice keyed by hand) | a measured, agreed share posted without a person | rollout, on a real stream |
| Accuracy on the messier suppliers | none (no labelled set yet) | clears the agreed accuracy bar | Phase 0, on the labelled set |

> The labelled-set gate is the accuracy KPI clearing its bar before extraction goes live; the rollout gate is the straight-through KPI clearing its bar before you widen. Miss either and the call is to keep the messier suppliers on human review and automate the clean ones first.

**The decision.**
> Fund a 14-day MVP (priced with sales) that proves invoice extraction on your own documents and posts the results into your ERP. Modest run cost, EU-resident, and measured so you can widen it on evidence.

**Closing hero boxes (Brückner):**

| Box | Value | Sub-line |
|---|---|---|
| **The build** | Invoice extraction MVP | One document type, real stream |
| **Effort** | 14 days | person-days, incl. Phase 0 |
| **Timeline** | ~5 wks | elapsed |
| **Indicative price** | priced with sales | + ~€800/mo run |

> The published example PDF shows the price as ~€20k. That is the published illustration only; the kit sizes the 14 person-days and the run cost, and the one-off price is compiled with sales at their rate.

---

## Report generator field map

**The form is the only input; the PDF is deterministic.** This is the **field spec the report generator should be built to** for the AI Kickstart (route `/new/kickstart`), section by section, mapped to the kit artifact each field is sourced from. The generator is pre-release; nothing has shipped, so there is no live form to preserve. It was drafted before the Kickstart was deepened (the go/no-go screen, the value & KPIs); **bring it up to this complete spec** rather than treating any of it as legacy. Use the map as a literal fill-in checklist too: work top to bottom, and for each field pull the answer from the artifact named. (Source files are relative to this folder.)

> Diagram and example handling: the **architecture diagram is uploaded separately** (off the critical path), and editable AWS templates live in the generator repo at `assets/diagram-templates/`. The output option **"Mark as EXAMPLE sample"** is what stamps EXAMPLE / illustrative / fictional-client on every page.

### Cover & basics

| Form field | Source artifact |
|---|---|
| **Client legal name** | `01-intake-questionnaire.md` (Section A: client name) |
| **One-line descriptor** (industry · size · location · cloud) | `01-intake-questionnaire.md` (Section A: industry, size, location, AWS/platform status) |

### Executive summary

| Form field | Source artifact |
|---|---|
| **Opening summary** | synthesised from D1–D5, "the short version": what they came to build, whether it fits, where the real work is |
| **Go/no-go read** · Proceed / Proceed with caution / Pause + any blocker named | `02-facilitator-runbook.md` (the go/no-go read); leads the page when Caution or Pause, otherwise sits quietly in the verdict |
| At-a-glance card · **VERDICT ON THE USE CASE** | D5 + D1 verdict (short verdict + qualifier) |
| At-a-glance card · **THE BUILD** | `03-facilitator-field-guide.md` (section 5 · Reference architecture: chosen pattern + stack in a phrase) |
| At-a-glance card · **INDICATIVE FIRST ENGAGEMENT** | `03-facilitator-field-guide.md` (section 4 · Cost basis, Headline: price · effort · timeline · run) |
| **Why it fits** | synthesised from D1 (Platform/People ready) + D2 (data/volume exists) |
| **What stands in the way** | synthesised from D2 (the 1–2 real gaps; note Phase 0 handles them) |
| **What to do first** | synthesised from D5 (the concrete first step) |
| **Honest-part callout** · heading + body | synthesised: the "clear no beats an expensive maybe" line (heading + body) |

### Deliverable 01 · Readiness snapshot

*Source: `03-facilitator-field-guide.md` (section 1 · Readiness snapshot). Three cards, each a **status label**, not a 0–5 score. Allowed status values: Ready / Ready, with us alongside / Low burden / Partial / Gap.*

| Form field | Source artifact |
|---|---|
| Card 1 · **Status** + **Area** (Platform) + one/two lines | `03-facilitator-field-guide.md` (section 1, Card 1 Platform: status + note) |
| Card 2 · **Status** + **Area** (People) + one/two lines | `03-facilitator-field-guide.md` (section 1, Card 2 People: status + note) |
| Card 3 · **Status** + **Area** (Compliance) + one/two lines | `03-facilitator-field-guide.md` (section 1, Card 3 Compliance: status + note) |
| **Verdict callout** · heading + body | `03-facilitator-field-guide.md` (section 1, snapshot verdict; fold cross-sell to AI Readiness Workshop into the body where relevant) |

### Deliverable 02 · Use-case data check

*Source: `03-facilitator-field-guide.md` (section 3 · Data-check gate).*

| Form field | Source artifact |
|---|---|
| **Rows** = `What the build needs` · `State` · `Detail & what to do` (State = Usable/Partial/Messy/Blocker) | `03-facilitator-field-guide.md` (section 3, the worksheet) |
| **Callout** · heading + body | `03-facilitator-field-guide.md` (section 3, "What actually decides this") |
| **"If accuracy falls short" note** (optional) | `03-facilitator-field-guide.md` (section 3, "The honest call") |

### Deliverable 03 · Reference architecture

*Source: `03-facilitator-field-guide.md` (section 5 · Reference architecture). Diagram uploaded separately; editable AWS templates in the generator repo at `assets/diagram-templates/`.*

| Form field | Source artifact |
|---|---|
| **The straight-through path** | `03-facilitator-field-guide.md` (section 5, happy-path narrative) |
| **The exception / human-review path** | `03-facilitator-field-guide.md` (section 5, exception path; Guardrails, CloudWatch, IAM least-privilege, EU residency) |

### Deliverable 04 · Indicative cost estimate

*Source: `03-facilitator-field-guide.md` (section 4 · Cost basis).*

| Form field | Source artifact |
|---|---|
| **One-off delivery rows** = `Item` · `Basis` (person-days) · `Indicative` (compiled with sales) | `03-facilitator-field-guide.md` (section 4, Table A; delivery sizes Item + Basis, the euro is added with sales) |
| **Rate note** (optional) | the rate is sales-owned; do not assert a day rate in the kit |
| **Estimated monthly run cost rows** = `Line item` · `Assumption` · `€/month` | `03-facilitator-field-guide.md` (section 4, Table B) |
| **Run total** (€/mo range) | `03-facilitator-field-guide.md` (section 4, Table B, Total) |
| **Run total label** | `03-facilitator-field-guide.md` (section 4, e.g. "Modest-volume run") |
| **Cost callout** · heading + body (optional) | `03-facilitator-field-guide.md` (section 4, "Where the cost sits": the cost driver) |

### Deliverable 05 · Recommended first engagement

*Source: synthesised from D2–D4; structure per D5 above.*

| Form field | Source artifact |
|---|---|
| At-a-glance card · **THE BUILD** | `03-facilitator-field-guide.md` (section 5 · Reference architecture) + D5 |
| At-a-glance card · **EFFORT** | `03-facilitator-field-guide.md` (section 4 · Cost basis, Headline: person-days incl. Phase 0) |
| At-a-glance card · **TIMELINE** | `03-facilitator-field-guide.md` (section 4 · Cost basis, Headline: elapsed weeks) |
| At-a-glance card · **INDICATIVE PRICE** | compiled with sales (effort from `06` at the agreed rate); not set in the kit |
| **Scope** (bullets) | D5 structure above |
| **Out of scope for the MVP** (bullets) | D5 structure above |
| **What you get** (bullets) | D5 structure above |
| **Expected benefit** · prose (order of magnitude, no ROI) | `02-facilitator-runbook.md` (Value & success metrics) |
| **KPI table** · `Metric` · `Baseline` · `Target` · `When measured` | `02-facilitator-runbook.md` (Value & success metrics); the phase gates reference these KPIs |
| **Decision callout** · heading + body | D5 structure above ("the decision in front of you") |

### Off critical path / output options

| Form item | Handling |
|---|---|
| **Architecture diagram upload** | Uploaded separately; editable AWS templates at `assets/diagram-templates/` in the generator repo |
| Output option · **Mark as EXAMPLE sample** | Stamps EXAMPLE / illustrative / fictional-client on every page |

> Every figure carries the standard disclaimer: **illustrative ballpark, not a quote.**

---

## Generator field spec (bring the generator up to this)

The generator was drafted from an earlier, lighter cut of the Kickstart, before this deepening (the go/no-go screen, the value & KPIs). **Nothing has shipped, so there is no live form to preserve.** The generator simply needs updating to carry the fields the report now uses. The map above plus the short table below are that complete set; build the generator to match. The Kickstart is the fast, single-use-case format, so this stays small by design: a handful of fields, not the full-workshop machinery.

| Field | Where | Source | Type |
|---|---|---|---|
| Go/no-go read (Proceed / Proceed with caution / Pause) + named blocker | Exec summary | `02-facilitator-runbook.md` (the go/no-go read) | enum + optional blocker text |
| Readiness snapshot status, per lens | D01 | `03-facilitator-field-guide.md` (section 1 · Readiness snapshot) | enum (Ready / Ready, with us alongside / Low burden / Partial / Gap) per card; verdict callout |
| Solution shape (the chosen architecture pattern, the single use case's fit) | D03 | `03-facilitator-field-guide.md` (section 5 · Reference architecture) | enum (document extraction / RAG assistant / classification / generation) + designed-architecture note |
| Per-row data check | D02 | `03-facilitator-field-guide.md` (section 3 · Data-check gate) | repeatable rows: what the build needs / State (Usable / Partial / Messy / Blocker) / detail & what to do |
| Value & success metrics | D05 | `02-facilitator-runbook.md` (Value & success metrics) | an expected-benefit prose field + a KPI table (metric / baseline / target / when). The phase gates reference these KPIs. |

This is the full field set for the fast format, not a patch on a shipped form. Update the generator to it.
