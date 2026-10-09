---
name: gdpr-data-breach-triage
description: Triage suspected personal data breaches under the GDPR and assist with notification preparation. Use when privacy, DPO, or legal teams need to extract incident facts, distinguish initial alert from controller awareness, assess supervisory-authority notification and data-subject communication separately, identify decision-critical missing facts, or prepare an initial notification draft.
---

# GDPR Data Breach Triage and Notification

## Overview

Use this Skill to perform an initial GDPR personal-data-breach assessment from incident materials and prepare decision support for privacy, DPO, or legal teams. Start in guided intake when key facts are missing; switch to decision mode only when the case is ready or urgent. Produce an EDPB-template-aligned notification draft only when appropriate or explicitly requested.

Read the relevant reference file before making a conclusion:

- [gdpr-edpb-core-rules.md](references/gdpr-edpb-core-rules.md) for legal baselines;
- [breach-risk-factors.md](references/breach-risk-factors.md) for qualitative risk analysis;
- [edpb-scenario-cards.md](references/edpb-scenario-cards.md) for comparable fact patterns;
- [edpb-2026-template-map.md](references/edpb-2026-template-map.md) only when drafting the notification; use the bundled official EDPB DOCX as the field-order authority.

Use the output structures in `assets/` when formatting the three deliverables.

## Conversation modes

### Guided intake mode — default for incomplete cases

Use guided intake when the user provides only a partial incident description and has not explicitly requested a triage card or notification draft.

On the first response:

1. State one short provisional status, without a full legal analysis.
2. Use exactly these two blocks: `已记录` (no more than four confirmed or unknown facts) and `请按编号回复`.
3. Under `请按编号回复`, ask at most four numbered questions, in this priority order: role; T1 or the time personal-data impact was confirmed; data categories and approximate scope; evidence of disclosure/exfiltration plus recovery or attacker-access status.

On each later response:

1. State the newly recorded fact and how it changes the current path.
2. Keep a running `已记录` fact ledger; do not re-ask answered questions.
3. Under `请继续确认`, ask at most two numbered next decision-critical questions. Do not hide additional questions in prose, tables, examples, or action lists.
4. Do not repeat the full triage card, 72-hour action list, or legal explanation unless the user asks or a decision-mode trigger is met.

### Decision mode

Switch to decision mode when any of the following occurs:

- the user requests a triage card, notification draft, or concrete notification decision;
- T1 is supported and the 72-hour deadline is within 24 hours;
- the role, personal-data impact, and enough risk facts are known to support a reasoned decision.

In decision mode, produce the triage card and missing-facts list. Preserve the fact ledger and distinguish confirmed, estimated, assumed, and unknown items.

### Notification drafting mode

Switch to notification drafting mode when the user requests a draft, notification is recommended, or risk cannot be excluded and the deadline is within 24 hours. Before writing, read `assets/notification-draft.md`. Reproduce every official Field 1–126 marker in that exact order; use its English labels verbatim and add Chinese assistance only after the label. Do not replace, consolidate, skip, or re-order fields. For every unavailable or inapplicable field, write `[TO CONFIRM]` or `Not applicable — [reason]` rather than omitting it.

## Workflow

### 1. Extract and label facts

Extract facts from the user's description and supplied materials before asking questions. Label each material fact as:

- **Confirmed**: directly stated or supported by supplied evidence;
- **Estimated**: an explicitly identified approximation;
- **Assumption**: a working inference that requires confirmation;
- **Unknown**: not available from the materials.

Never invent dates, times, numbers, data categories, countries, recipients, access evidence, or remediation evidence. Do not ask for facts already supplied.

### 2. Identify the role

Classify the organisation as `controller`, `processor`, `joint controller`, or `unclear`.

If it is a processor, prioritize an action to notify the controller without undue delay. Do not require the processor to complete the controller's risk assessment, and do not treat the processor as the controller's supervisory-authority notifier without an identified legal or contractual basis.

### 3. Decide whether a personal data breach likely occurred

Assess whether the incident involved personal data and affected one or more of:

- confidentiality: unauthorised disclosure or access;
- integrity: unauthorised alteration or destruction;
- availability: loss of access or usability.

Return exactly one primary conclusion:

- **Likely personal data breach**;
- **Likely not a personal data breach**;
- **Insufficient facts to determine**.

Explain the facts supporting the conclusion and identify the material uncertainty.

### 4. Establish the time record

Keep these times separate:

- **T0 — initial alert**: first report or signal received;
- **T1 — controller awareness**: when the controller has a reasonable degree of certainty that a security incident resulted in a personal-data breach;
- **72-hour deadline**: calculate from T1 only when T1 is sufficiently supported.

Do not substitute management approval, completion of forensic investigation, or a later meeting for T1. If T1 is uncertain, show the uncertainty and state what evidence is needed; do not fabricate a deadline.

### 5. Ask only decision-critical questions

List only missing facts that could change one of the three decision gates. Prioritize:

- role and controller identity;
- T0, T1, and whether the incident is ongoing;
- confidentiality, integrity, or availability impact;
- data categories and approximate scope;
- data-subject categories and vulnerable people;
- recipient, attacker, or other access party;
- evidence of access, download, disclosure, exfiltration, or further use;
- encryption, pseudonymisation, deletion confirmation, recovery, and other effective mitigations;
- likely consequences and affected countries.

For each question, state why it matters and the likely source or owner. In guided intake, follow the question caps in the conversation-mode rules; give a decision deadline only when it is supported by the materials.

### 6. Assess risk qualitatively

Use the factors in `references/breach-risk-factors.md`. Consider severity and likelihood together. Do not use a numerical score as a substitute for reasoning. State risk-increasing factors, risk-reducing factors, evidence quality, and unresolved facts.

### 7. Make three separate decisions

Return one conclusion for each gate:

1. **Breach gate**: likely breach / likely no breach / insufficient facts;
2. **Supervisory-authority gate**: no current notification but record / notification recommended / prepare phased notification / insufficient facts by a stated review point;
3. **Data-subject gate**: communication not currently indicated / likely high risk and communication recommended / revisit after facts / possible Article 34(3) exception requiring verification.

Do not collapse the second and third gates. A decision not to notify the authority must still include an internal-record recommendation and reasons.

### 8. Produce the deliverables

In decision mode, produce:

1. a **GDPR breach triage card**;
2. a **decision-critical missing-facts list**.

Produce a **supervisory-authority notification draft** only when notification is recommended, risk cannot be excluded and the review point is near, or the user explicitly requests it. Before delivering, run this checklist: Field 1 through Field 126 appear once, in order; every conditional field is completed, marked `[TO CONFIRM]`, or marked `Not applicable — [reason]`; the 2026 template is identified as consultation-stage; no local DPA or portal is invented.

### 9. Close with human review

State that the result is preliminary decision support, not a final legal opinion or filing. Require confirmation by the privacy team, DPO, legal team, or authorised controller representative before external notification or data-subject communication.

## Guardrails

- Keep GDPR-only scope; flag other jurisdictions or sectoral duties as outside V0.1.
- Do not wait for complete forensics before assessing whether notification may be required.
- Do not call the 2026 EDPB template a final or universally implemented DPA form.
- Do not invent a supervisory authority, lead authority, portal, or local deadline.
- Do not generate a notification draft when the facts do not support a meaningful draft unless the user explicitly asks for a clearly marked placeholder draft.
- Preserve the distinction between law, EDPB guidance, and internal recommendations.
- Do not skip, rename, reorder, or replace EDPB template fields in notification drafting mode. Use `[TO CONFIRM]` or the official incomplete-notification options where facts are unavailable.
