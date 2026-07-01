# 01 · Intake Questionnaire (Client Pre-work)

**AI Kickstart · superluminar GmbH**

You already know what you want to build. This pre-work captures **one use case**, the **data behind it**, and just enough about your platform and people for us to take a quick readiness read. It's deliberately short, 30–45 minutes. The honest detail you give us here is what lets us pressure-test the use case in the session rather than spend the session gathering facts.

> If you find yourself wanting to describe *several* things you might build, that's a sign the **AI Readiness Workshop** fits better. Tell us and we'll point you there.

Fill in the fields. "Don't know" is a perfectly good answer; it tells us where to dig.

---

## Section A · Who's completing this

| Field | Your answer |
|---|---|
| Company | |
| Industry / what you make or do | |
| Approx. employees | |
| Primary AWS region in use | |
| Completed by (name, role) | |
| Date | |

---

## Section B · The one use case

Describe the single thing you want to build. One use case only.

| Question | Your answer |
|---|---|
| In one sentence, what do you want to build? | |
| What problem does it solve, and for whom? | |
| How is this done today (manual process / tool / not at all)? | |
| Who feels the pain most? (team, role) | |
| What does success look like in numbers? (e.g. hours saved, % automated) | |
| Is this **assist** (helps a person) or **decide** (acts on its own)? | |
| Rough volume (documents/queries/items per day or month) | |
| Is there a deadline or trigger pushing this now? | |

**Pattern check.** Which best describes it? (tick)
- [ ] **Document extraction:** pull structured fields out of documents (invoices, forms, contracts)
- [ ] **Q&A / assistant (RAG):** answer questions over your own documents/knowledge
- [ ] **Classification / routing:** sort or tag incoming items
- [ ] **Generation / drafting:** produce text from inputs
- [ ] **Other (describe):** ______________________________

---

## Section C · The data behind it (the part that decides it)

This is what we pressure-test. Be honest about the messy bits; that's the point.

| Question | Your answer |
|---|---|
| What data does this use case need to work? | |
| Where does it live today? (system, S3, email, file shares, ERP, …) | |
| Roughly how much is there, and how far back? | |
| Format(s)? (PDF scans, digital PDFs, images, DB rows, text…) | |
| How consistent is it? (one format vs many; clean vs variable quality) | |
| Is there a **labelled / ground-truth** set we could measure accuracy against? Where would correct answers come from? | |
| Who owns this data internally? | |
| Any data that is personal, sensitive, or regulated in here? | |
| Where must the data stay? (EU-only? specific region?) | |

---

## Section D · Where it has to plug in (integration)

| Question | Your answer |
|---|---|
| What system must the result land in? (ERP, CRM, ticketing, DB…) | |
| Is there a clean, permissioned way to write/read it today (API)? Or is it manual? | |
| Who owns that target system internally? | |

---

## Section E · Platform (lens 1, light)

| Question | Your answer |
|---|---|
| Are you on AWS today? Which region(s)? | |
| Roughly how mature is your AWS setup? (accounts, IAM, CI/CD, IaC) | |
| Have you used Bedrock / Textract / Step Functions before? | |
| Any landing-zone, networking or account constraints we should know? | |

---

## Section F · People (lens 2, light)

| Question | Your answer |
|---|---|
| Who would own this in production after we leave? | |
| Do you have engineers who'd build alongside us? | |
| Anyone ML/AI-aware in-house? | |
| How keen is the team that feels the pain to change the process? (low / mixed / high) | |

---

## Section G · Compliance (lens 3, light)

| Question | Your answer |
|---|---|
| Does this use case touch personal data (GDPR)? Roughly how much? | |
| Does it **decide about people** (eligibility, scoring, HR, credit…)? | |
| Any sector regulation that applies? (finance, health, public sector…) | |
| Any existing data-residency or security policy we must honour? | |

---

## Section H · Anything else

Constraints, prior attempts, hard "no"s, internal politics, budget shape: whatever helps us read the situation honestly.

```
[free text]
```

---

## Bring to the session

A few real things, scoped to the one use case, that let the room go deep instead of speculating. Redact freely; we need shape, not secrets.

- [ ] **A handful of sample documents or records** the use case would actually run on (redacted), spanning the clean and the messy cases.
- [ ] **Where the correct answers live today:** the ERP values, an existing labelled or checked set if you have one, or simply who currently does the task by hand.
- [ ] **The target system** the result must land in (ERP, CRM, ticketing, DB), and whoever knows its integration reality.
- [ ] **The AWS region** you run in (or intend to).

---

## In the room, go deeper

A short set we'll push on live. Bring evidence, not estimates.

- **The number.** Real volume and frequency, not "a lot". How many per day or month, and how variable?
- **"Good enough to ship".** What accuracy or coverage has to be true for this to go live? Who decides that bar?
- **Where the data actually lives, and who can read it.** Show us the system. Who has permissioned access today?
- **The write path.** Is there a clean, permissioned way to land results in the target system? Who can confirm it exists?

---

*Return this to us before the session. We read it in advance so the session is spent pressure-testing, not gathering. All figures and recommendations in the resulting report are illustrative ballparks, not a quote.*
