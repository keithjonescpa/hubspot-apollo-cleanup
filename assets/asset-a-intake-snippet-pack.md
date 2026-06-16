# ASSET A — Intake Snippet Pack (Scripts 1–7)

**TheCPATaxProblemSolver™ · Tax Controversy Intake & Investigation**
*Solving Bad Tax Problems for Good People™*

-----

## DEPLOYMENT HEADER

- **Surface:** HubSpot Snippets (call templates) → Canopy task checklists → M365 Loop plan
- **Owners:** Discovery/close = TheCPATaxProblemSolver™ · Intake & launch checklists = Intake Specialist / Case Manager role
- **Compliance anchors:** Circular 230 §10.30 (no misleading solicitation/no guarantees), §10.27 (fees), §10.28 (records), §10.21 (client omissions); IRS Pub 4557 §III (safeguards); IRC §7216 (TP info use/disclosure consent)
- **Hard rules:** No real name, no full SSN, no full transcript data in any stored template. Tokens only. Documents move through the **client portal**, never email. Role labels in templates — personal names only in DMs, engagement letters, 2848/8821/DR-835.

### MERGE TOKEN DICTIONARY (use everywhere — keep identical across Assets A/B/C)

| Token                               | Source                                        | Note                                                                                                                                 |
|-------------------------------------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `{{rep_name}}`                      | HubSpot owner (active ID 84310740)            | —                                                                                                                                  |
| `{{rep_credential}}`                | Contact/Deal prop `rep_credential` (CPA \| EA) | Never hardcode "CPA"                                                                                                               |
| `{{caf_number}}`                    | 1Password secure field                        | Never in HubSpot plaintext                                                                                                         |
| `{{taxpayer_ref}}`                  | Initials only                                 | No full name in template                                                                                                           |
| `{{tin_last4}}`                     | Encrypted prop `tin_last4`                    | Last 4 only                                                                                                                        |
| `{{agency}}`                        | Deal prop (IRS \| FDOR \| Both)                | Drives branch                                                                                                                      |
| `{{phase1_fee}}` / `{{phase2_fee}}` | Deal props                                     | Flat fee                                                                                                                           |
| `{{case_manager}}`                  | Owner/role                                     | —                                                                                                                                  |
| `{{update_cadence}}`                | Deal prop (e.g., "every 3 weeks")             | —                                                                                                                                  |
| `{{portal_link}}`                   | Canopy portal URL                             | Docs go here, not email                                                                                                           |
| `{{doc_deadline}}`                  | Date prop                                      | —                                                                                                                                  |
| `{{firm_disclaimer}}`               | Snippet                                        | "Keith L. Jones, CPA is a licensed Florida CPA (#AC0028367). No tax or legal advice is offered until a formal engagement is signed." |

-----

## SNIPPET 1 — Tax Resolution Intake / Discovery Call

*HubSpot snippet shortcut suggestion: `#intake-discovery`*

**Open & Authority (60–90 sec)**

- "You're in the right place. I work IRS and Florida tax controversy matters all day, every day."
- "I'll ask pointed questions, then tell you your realistic options and what it takes to fix this."
- "If it's a fit, I'll outline what working together looks like. If it's not, I'll tell you that too."

**⚠️ DISCLOSURE BEAT (mandatory — say before any strategy talk):**

- "Before I outline options — nothing I say today is a guaranteed result. The IRS and the Florida Department of Revenue control final outcomes. What you get from me is a firm recommendation and a written plan once we're engaged."

**Fast Context & Control**

- "What notice or problem pushed you to call today — specifically?"
- "Roughly how much do you think you owe, and to whom — IRS, FDOR, or both?"
- "Which years are in play? Best guess — we verify with transcripts."

**Compliance & Risk Snapshot**

- "Are your last six years of returns filed — yes, no, or not sure?"
- "Any active levies or wage garnishments right now?"
- "Ever had an installment agreement, Offer in Compromise, or penalty abatement approved or denied?"

**Ability to Pay & Reality Check**

- "If they said 'pay $X a month to stop enforced collection,' what's honestly doable without wrecking your life?"
- "Is anyone else trying to fix this right now — another firm, a friend, or you on your own?"

**Qualify & Pivot**

- *If viable:* "You qualify as a serious case. Real risks, real options. My process has two phases — Phase 1 is investigation and protection; Phase 2 is execution. Let me walk you through Phase 1."
- *If not viable:* "Blunt truth: hiring me isn't a good use of your money right now. Here's what you can do yourself to get stable."

**Close (if yes)**

- "Let's walk through Phase 1 — what you get and how the fee works. Then you decide if you want me in your corner."
- `{{firm_disclaimer}}`

> **Owner:** TheCPATaxProblemSolver™ · **KPIs:** Scheduled→Qualified %, Qualified→Phase 1 %, no-show rate, call length

-----

## SNIPPET 2 — Case Interview Checklist (Internal — Canopy task)

*Run live during discovery. Yes/No + notes. No full PII in notes — use `{{taxpayer_ref}}`.*

- [ ] **Jurisdiction:** IRS only · IRS + FDOR · FDOR only
- [ ] **Notices on hand:** CP504 · LT11/LT1058/CP90 · RO assigned · ACS · (FDOR: DR-840 · NOPA · NOFA · warrant)
- [ ] **Years + status:** list years; filed / unfiled each
- [ ] **Current enforcement:** wage levy · bank levy · garnishment · passport · license risk
- [ ] **Prior resolutions:** IA · CNC · OIC · FTA · rejections (dates)
- [ ] **Financial snapshot:** income sources · W-2 vs SE · assets w/ equity · hardships
- [ ] **Deadlines:** levy dates · response deadlines · RO meeting · **FDOR protest/contest dates (from face of notice)**
- [ ] **Red flags (§10.21):** fraud risk · unreported income · ghost preparer · prior practitioner issue · collected-but-unremitted trust funds

> **Owner:** Intake Specialist · **KPIs:** Checklist completion %, missing-data rate post-intake, time-to-Phase-1 decision

-----

## SNIPPET 3 — Phase 1 Engagement Discussion Guide

*Shortcut: `#phase1-pitch`*

- **Frame:** "Right now the IRS sees a file, not a human being. They act on what's in that file."
- **What Phase 1 is:** "We pull every transcript, decode what they have, stop surprises, and build the strategy. That's where I earn the right to tell you what actually works."
- **Deliverables (plain language):** full account + wage & income transcripts · filing-compliance map · collections risk assessment (levy risk, timelines) · written game plan with top 1–2 viable options
- **Fee & decision ask:** "Phase 1 is a flat **$`{{phase1_fee}}`**. No payment, no work — I'm putting my name and license on this. Phase 2 is a separate agreement; today's decision is only Phase 1."
- **Close:** "Given the levy risk and penalties still running — ready to lock in Phase 1 so I can start pulling transcripts?"
- `{{firm_disclaimer}}`

-----

## SNIPPET 4 — Phase 2 Engagement Discussion Guide

*Shortcut: `#phase2-pitch`*

- "We've completed Phase 1. You've seen your transcripts, risk map, and options."
- "Recommendation: **[OIC / IA / CNC / PPIA / penalty abatement]**, because [one-line rationale]."
- "Phase 2 is execution — we prepare forms, build the financial package the IRS expects, and own all contact with ACS / RO / Appeals."
- "Fee is a flat **$`{{phase2_fee}}`** — not an hourly experiment. That's the cost for me to own the process and protect you."
- "Ready for me to take this off your plate and own the IRS conversations from here?"
- `{{firm_disclaimer}}`

-----

## SNIPPET 5 — Case Launch Checklist (Internal — Canopy)

*Trigger: Phase 2 signed + paid. Target: launch within 1 business day.*

- [ ] POA filed — **2848 / 8821 (IRS)** or **DR-835 (FDOR)**
- [ ] Case built in Canopy with phases + tasks
- [ ] "Welcome + What Happens Next" email sent
- [ ] Document request list sent via **`{{portal_link}}`** with `{{doc_deadline}}`
- [ ] Case calendar: controlling deadlines, IRS/FDOR follow-ups, client update cadence `{{update_cadence}}`
- [ ] Risk flags logged: levy risk · RO/auditor behavior · special issues
- [ ] IRC §7216 consent captured if any info will be used/disclosed beyond the engagement

> **Owner:** Case Manager · **KPIs:** % launched ≤1 business day, % with complete checklist, "where are we?" call count

-----

## SNIPPET 6 — Case Manager Introductory Call

*Shortcut: `#cm-intro`*

- "I'm `{{case_manager}}`, your day-to-day contact. My job: nothing slips, and you know what's happening before you have to ask."
- "From you: answer our emails, upload documents to the portal, tell us if income or address changes."
- "From us: a status update at least `{{update_cadence}}` — even if the IRS hasn't moved."
- "If you're worried, contact me directly. Do **not** call the IRS behind our back — it can derail the strategy."

-----

## SNIPPET 7 — Explaining Resolution Timelines

*Shortcut: `#timelines`*

- "The IRS moves on IRS time — months, not days."
- "Three clocks run: your **risk clock** (levy/lien), the **IRS processing clock**, and our **work clock** (how fast you get us what we need)."
- "A typical [OIC/IA/etc.] runs roughly [range] start to finish. I can't make the IRS faster — I can make your case clean, complete, and pushed at the right moments."
- "If we hit unusual delays, you hear it from us first — not from a letter."

> **Note:** Keep the [range] as a *general* expectation, never a promise. Current IRS processing times shift — verify before quoting a specific month count.

-----

## HUBSPOT WORKFLOW LOGIC (native-first)

### Pipeline: `Tax Controversy — Intake & Investigation`

| Stage                             | Entry condition                 | Snippet to attach   | Internal action                                                   |
|-----------------------------------|---------------------------------|---------------------|-------------------------------------------------------------------|
| 1. New Lead                       | Form/Quo intake created         | —                   | Auto-assign owner; lead-response timer starts                     |
| 2. Discovery Scheduled            | Meeting booked                  | `#intake-discovery` | Reminder + no-show task                                           |
| 3. Discovery Held — Qualified     | `discovery_outcome = Qualified` | `#phase1-pitch`     | Create Canopy interview checklist (Snippet 2)                     |
| 3b. Discovery Held — Disqualified | `discovery_outcome = DQ`        | self-help nurture   | Close-lost reason logged                                          |
| 4. Phase 1 Proposed               | Proposal sent                   | —                   | Follow-up sequence (Day 1/3/7)                                    |
| 5. Phase 1 Signed                 | Engagement signed + paid        | —                   | Launch transcripts task                                           |
| 6. Investigation                  | Transcripts in                  | —                   | Build game plan                                                   |
| 7. Phase 2 Proposed               | Plan delivered                  | `#phase2-pitch`     | Follow-up sequence                                                |
| 8. Phase 2 Signed                 | Engagement signed + paid        | `#cm-intro`         | Fire Case Launch Checklist (Snippet 5); hand to Delivery pipeline |

### Required deal properties

`agency` · `discovery_outcome` · `rep_credential` · `tin_last4` (encrypted) · `phase1_fee` · `phase2_fee` · `update_cadence` · `controlling_deadline` · `levy_risk` (Low/Med/High)

### Workflows to build (HubSpot native)

1. **Lead-response timer** — start at Stage 1; alert owner if no first touch in target window (KPI: lead response time).
2. **No-show recovery** — if meeting `no-show`, enroll in 3-touch rebook sequence.
3. **Phase 1 / Phase 2 follow-up** — Day 1/3/7 task + email reminders until signed or close-lost.
4. **Stalled-deal escalation** — deal idle in any stage > threshold → notify `{{case_manager}}`.
5. **Launch trigger** — Phase 2 signed → create Canopy case + Snippet 5 checklist + Welcome email.

### KPI dashboard (HubSpot report)

Booked calls · Show rate · Qualified % · Phase 1 conversion % · Phase 2 conversion % · Avg case value · Pipeline velocity (days/stage) · Lead response time · Intake checklist completion %

-----

## ⚠️ COMPLIANCE & IP NOTES

- **§10.30:** Disclosure beat (Snippet 1) + `{{firm_disclaimer}}` neutralize guarantee/misleading risk. Do not strip them.
- **Pub 4557 §III / §7216:** Documents through portal only; capture §7216 consent before any third-party or AI use of taxpayer info.
- **IP:** This two-phase tokenized intake system is a packageable module ("Signal-to-Signed™" adjacent). Run a USPTO knockout before applying ™/® to any new mark coined here.
