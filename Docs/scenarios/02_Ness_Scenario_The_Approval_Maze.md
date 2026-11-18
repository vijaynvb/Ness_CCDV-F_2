# Ness AI Engineering Challenge 02
## The Approval Maze — Programme Decision & Approval Register

**Audience:** AI Engineering training participants  
**Suggested team size:** 3–5 participants  
**Exercise type:** Vibe coding / AI-assisted application development  
**Suggested duration:** 2–3 hours  
**Role:** You are an AI engineering squad supporting a Ness programme delivery team.

> This is a simulated business scenario adapted from the supplied Applied AI Studio material. All organisation and engagement details are fictionalised for the exercise.

## 1. Business context

A Ness programme delivery team is managing a complex transformation programme for a large enterprise client. Key decisions are spread across email threads, meeting notes and individual spreadsheets.

The same topics are repeatedly discussed at steering committee meetings because nobody can quickly establish:

- What decision was required.
- Who was accountable for making it.
- What options were considered.
- Whether the decision was approved, rejected or deferred.
- What actions followed from the decision.

The client has formally escalated the issue. The programme team is spending time reconstructing decision history instead of moving delivery forward.

### Illustrative symptoms

- Decisions are re-debated across multiple steering committee meetings.
- Approval chains are difficult to understand.
- Decision owners and due dates are not consistently recorded.
- Some items remain pending without a clear escalation path.
- Client and internal stakeholders have different understandings of the status.

## 2. The trigger event

The client has asked Ness to demonstrate a more transparent and accountable way of managing programme decisions before the next steering committee.

The programme director needs a working prototype that can be used to log decisions, assign a single accountable owner, track approval status and record the outcome.

## 3. Your assignment

Build a **Programme Decision & Approval Register** that creates visibility and accountability without turning every decision into a lengthy administrative exercise.

### Required capabilities

1. **Decision dashboard**
   - Total decisions.
   - Pending, in-review, approved, rejected and deferred counts.
   - Overdue decisions.
   - Decisions due in the next seven days.

2. **Decision register**
   - Create, edit and view decisions.
   - Capture a unique decision ID, title, description and category.
   - Capture request date, required-by date and status.
   - Assign one accountable decision owner.
   - Record contributors or consulted stakeholders separately from the accountable owner.
   - Capture priority and programme/workstream.

3. **Approval workflow**
   - Define approval stages or approver roles.
   - Record approval status, approver, date and comments.
   - Prevent a decision from being marked approved unless required approval information is present.
   - Support rejected, deferred and returned-for-clarification outcomes.

4. **Decision history**
   - Record status changes and key updates.
   - Capture rationale and outcome summary.
   - Show the latest update and who made it.
   - Make overdue decisions and ownership gaps visible.

5. **Escalation and reporting**
   - Highlight overdue decisions.
   - Show decisions awaiting a specific approver.
   - Provide filters for status, owner, priority and workstream.
   - Provide a client-facing summary view that can be distinguished from the internal working view.

6. **Usability**
   - A clean, responsive interface.
   - Fast decision creation and closure.
   - Search and filter controls.
   - Sample data that demonstrates a realistic programme.
   - Clear validation and empty states.

## 4. Constraints and non-goals

The prototype must:

- Be a self-contained browser-based application for the exercise.
- Use synthetic programme and stakeholder data.
- Demonstrate the workflow without sending real approval emails or changing enterprise records.
- Clearly label simulated actions and sample data.

The prototype must **not**:

- Be represented as a formal contractual record or legally binding approval system.
- Replace the client's official programme governance process.
- Store privileged legal advice, sensitive commercial negotiation content or personal data.
- Send notifications, approve spend or trigger external actions.
- Claim to provide identity verification, non-repudiation or a tamper-proof audit trail.

## 5. Business and governance decisions your team must make

Before building, agree and document:

1. Is this an internal coordination tool, a client-visible status tool, or both with role-appropriate views?
2. Who is the single accountable owner for each decision?
3. Which decision categories require a separate formal approval process?
4. What information is mandatory before a decision can be closed?
5. What should happen when a decision is overdue?
6. Which fields and history are visible to the client?
7. What retention and ownership arrangements would apply after the programme closes?

The tool should make accountability clear while avoiding the capture of unnecessary or sensitive information.

## 6. Build approach

Keep one AI coding conversation open throughout the exercise.

### Stage A — Frame the problem
Write a product brief that defines:
- Users and roles.
- Decision lifecycle and status transitions.
- Data model and mandatory fields.
- Internal versus client-facing information.
- Non-goals and governance boundaries.
- Acceptance criteria.

### Stage B — Build
Ask the AI coding assistant to build a working register. Prioritise creating, assigning, updating, approving and closing a decision.

### Stage C — Iterate
Complete at least two meaningful iterations. Examples:
- Enforce one accountable owner.
- Add approval-stage validation.
- Add overdue calculations and escalation cues.
- Improve the decision history.
- Separate internal and client-facing summaries.

### Stage D — Test
Test the full lifecycle, invalid transitions, missing owners, overdue decisions, rejected decisions and client-view filtering.

### Stage E — Interrogate and govern
Ask the AI assistant to identify ways the register could be bypassed, gamed or misused. Decide what the application can enforce and what must remain a programme process or formal control.

## 7. Acceptance criteria

The prototype is ready to present when:

- A user can create, edit, search and filter decisions.
- Every active decision has one accountable owner.
- Status transitions follow defined rules.
- Approval cannot be recorded as complete without required details.
- Overdue decisions are calculated from dates and status.
- A decision history is visible in the prototype.
- Client-facing information is clearly separated from internal-only information.
- Sensitive categories are excluded or redirected to the appropriate formal process.
- The application clearly states that its history is a prototype record, not a tamper-proof audit log.
- The team can explain what would be required for production use.

## 8. Presentation

Prepare a **5–7 minute demonstration** covering:

1. The business problem and target users.
2. Creating a decision and assigning its accountable owner.
3. Moving the decision through approval and closure.
4. How overdue decisions and escalation are surfaced.
5. Two meaningful AI-assisted iterations.
6. Governance decisions: formal versus informal use, access, retention, ownership and production gaps.

## 9. Questions for the team

- Does the tool make it easier to close a decision than to leave it pending?
- Can a decision have multiple contributors but only one accountable owner?
- What happens when an approver is unavailable?
- Could users use vague wording to avoid accountability?
- What information should never appear in the client-facing view?
- What controls are needed before this becomes part of formal programme governance?
