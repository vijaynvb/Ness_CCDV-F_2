# Ness AI Engineering Challenge 01
## The Invisible Close — Month-End Close Visibility Dashboard

**Audience:** AI Engineering training participants  
**Suggested team size:** 3–5 participants  
**Exercise type:** Vibe coding / AI-assisted application development  
**Suggested duration:** 2–3 hours  
**Role:** You are an AI engineering squad supporting a Ness Finance & Accounting delivery engagement.

> This is a simulated business scenario adapted from the supplied Applied AI Studio material. All organisation and engagement details are fictionalised for the exercise.

## 1. Business context

Ness operates the end-to-end Finance and Accounting function for a global manufacturing client. The engagement processes approximately **14,000 transactions per month** across:

- Accounts Payable (AP)
- Accounts Receivable (AR)
- General Ledger (GL) reconciliation
- Intercompany
- Month-End Journal Entries

The work is delivered from a Ness centre in Hyderabad. The team has **38 associates**, managed by four delivery leads.

Month-end close runs over five business days. Progress is currently tracked in a shared Excel workbook maintained manually by three senior analysts. Each analyst extracts information from SAP, updates their section and emails a consolidated workbook to the delivery lead at 6 p.m.

By the time leadership receives the consolidated view, the information is typically **18–24 hours old**. Reconciliation exceptions are discussed in separate email threads and are not visible to everyone who needs them.

The engagement is 26 months old, profitable and due for renewal in Q3. The client's CFO has begun asking increasingly detailed questions during quarterly reviews.

## 2. The trigger event

During Day 4 of the previous quarter's close, the client's CFO asked the Ness Delivery Head:

> “What percentage of GL reconciliations are complete right now?”

It took **47 minutes and four phone calls** to provide an answer. The CFO responded that this was not acceptable.

At the following week's review, the CFO stated:

> “I should be able to look at a screen and see where we are at any given moment. If your team cannot answer in 60 seconds, I do not have confidence in the process — and that matters for the renewal conversation.”

### Current pain points

| Measure | Current state |
|---|---:|
| Time to answer a real-time close question | 47 minutes |
| Tracker information delay | 18–24 hours |
| Senior analysts maintaining manual updates | 3 |
| Daily time spent by each analyst on updates | 90+ minutes |

## 3. Your assignment

Build a **Month-End Close Visibility Dashboard** that gives delivery leadership and authorised client stakeholders a clear view of close progress across all five workstreams.

The prototype must be usable by the end of this exercise. It should demonstrate how AI engineering can turn a loosely defined business problem into a working, testable application.

### Required capabilities

1. **Executive summary**
   - Overall close completion percentage.
   - Total tasks, completed tasks, in-progress tasks and blocked/exception tasks.
   - Current close day and reporting timestamp.

2. **Workstream view**
   - AP, AR, GL Reconciliation, Intercompany and Journal Entries.
   - Completion percentage and status for each workstream.
   - Clear visual indication of at-risk or blocked workstreams.

3. **Task and exception management**
   - Add or update a task.
   - Capture task owner, due date, status and workstream.
   - Record an exception summary, severity, owner and target resolution date.
   - Filter tasks and exceptions by workstream, status and severity.

4. **Progress trends**
   - Show progress by close day or reporting period.
   - Highlight overdue and unresolved items.
   - Make it easy to identify where leadership intervention is required.

5. **Usability**
   - Responsive desktop and mobile layouts.
   - Executive-friendly design, readable in under two minutes.
   - Clear labels, sensible empty states and sample data.
   - Provide a simple way to reset or reload demo data.

## 4. Constraints and non-goals

The prototype must:

- Be a browser-based application that can be demonstrated without a server.
- Use synthetic/sample data only.
- Support manual updates by the delivery team.
- Be suitable for a controlled demonstration to client stakeholders.
- Be achievable within the exercise timebox.

The prototype must **not**:

- Connect directly to SAP or any production system.
- Store raw financial transaction data, bank details, employee personal data or client-confidential records.
- Claim to provide a true real-time view when updates are manual.
- Be represented as an approved production system or formal financial record.
- Bypass Ness or client security, architecture, data governance or change-control processes.

## 5. Business and design decisions your team must make

Before building, agree and document:

1. Should the client see the full operational view, a curated summary, or a daily snapshot?
2. How will the dashboard distinguish an operational warning from an issue requiring escalation?
3. How will the UI make the freshness of manually entered data unmistakable?
4. Which fields are mandatory when a task is marked blocked or completed?
5. What is explicitly outside the prototype's scope?
6. Who would own and maintain a future governed version?

There is no single prescribed answer. Your team must explain its trade-offs.

## 6. Build approach

Use your AI coding assistant as a collaborator. Keep the same conversation open through the build and refinement stages.

### Stage A — Frame the problem
Write a short product brief covering:
- User personas and decisions they need to make.
- Required features and non-goals.
- Data fields and business rules.
- UX expectations and acceptance criteria.
- Security, privacy and governance constraints.

### Stage B — Build
Ask the AI coding assistant to create the application. Start with a working end-to-end flow rather than polishing isolated screens.

### Stage C — Iterate
Complete at least two meaningful iterations. Examples:
- Correct the calculation of overall completion.
- Improve exception filtering and escalation visibility.
- Add data freshness indicators and validation.
- Improve mobile usability and accessibility.

### Stage D — Test
Use realistic synthetic data. Test normal, edge and error cases. Do not accept a generated application simply because it renders.

### Stage E — Interrogate and govern
Ask the AI assistant to review the prototype for failure modes, privacy risks, misleading metrics and operational misuse. Decide which recommendations to adopt.

## 7. Acceptance criteria

The prototype is ready to present when:

- All five workstreams are visible.
- Overall completion is calculated from underlying task data, not hard-coded.
- Task and exception updates change the relevant metrics and views.
- Filters work and can be cleared.
- Blocked and overdue items are easy to identify.
- Data freshness and manual-entry limitations are visible.
- Invalid or incomplete entries are handled clearly.
- The application works at desktop and mobile widths.
- The team can explain what is simulated, what is not integrated and what would be required for production.

## 8. Presentation

Prepare a **5–7 minute demonstration** covering:

1. The business problem and target users.
2. The working dashboard and one end-to-end update.
3. Two important iterations made with the AI assistant.
4. Tests performed and defects or limitations discovered.
5. Governance decisions: ownership, access, data boundaries, retention and production-readiness gaps.

## 9. Questions for the team

- Does the dashboard help the CFO make a decision, or merely display more numbers?
- What happens if a workstream owner does not update the tracker?
- How will the user know whether a red status is current or stale?
- Could a manually entered percentage create false confidence?
- What controls would be required before connecting this prototype to SAP?
