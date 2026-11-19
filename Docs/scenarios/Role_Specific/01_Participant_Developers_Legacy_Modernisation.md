# Ness AI Engineering Challenge 01 — Developers
## Legacy Modernisation & Intelligent Code Engineering

**Role:** Ness application development team | **Team size:** 3–5 | **Duration:** 3–4 hours

> Fictional training scenario. Use synthetic code, sample data and non-production systems only.

## 1. Business context

Ness supports a customer-facing order management platform for a global distribution company. The platform has evolved over eight years and consists of Customer API (.NET Core), Order API (Java Spring Boot), Inventory service (Node.js), Notification service (Node.js), PostgreSQL and Redis.

The platform is operational, but changes are increasingly difficult. Documentation is incomplete, original developers have moved on, and business rules are duplicated across services.

The client has requested **Partial Order Fulfilment**: available items should ship while unavailable items remain pending. The current implementation assumes an order is fulfilled as a single unit.

## 2. Trigger event

A recent enhancement caused an inventory inconsistency: an order was marked fulfilled although one item was unavailable. The team spent two days tracing duplicated business rules and service interactions.

The client wants Ness to demonstrate a safe AI-assisted approach to understanding the codebase and implementing the feature without regressions.

## 3. Your assignment

Design and prototype a **Developer Engineering Copilot workflow** that helps a developer:
1. Understand an unfamiliar multi-service codebase.
2. Identify affected services, APIs, data models and business rules.
3. Propose a safe implementation plan.
4. Implement the change with tests.
5. Review code for defects, security concerns and unintended changes.
6. Produce developer documentation and a pull-request summary.

Use a sandbox repository, or create a small representative multi-service repository if none is supplied.

## 4. Required capabilities

### Repository understanding
- Summarise service responsibilities and dependencies.
- Identify relevant endpoints, domain models, database entities and tests.
- Trace the order lifecycle across services.
- Cite file paths and code locations for findings.

### Change impact analysis
- Accept a feature request in natural language.
- Identify impacted services, APIs, tables/events and tests.
- List assumptions, risks and questions requiring developer confirmation.
- Produce a plan before editing code.

### AI-assisted implementation
- Implement partial fulfilment for the agreed scope.
- Preserve existing full-fulfilment behaviour.
- Add/update unit and integration tests.
- Include validation, error handling and meaningful logs.
- Avoid unrelated refactoring.

### Code review and documentation
- Review diffs for correctness, maintainability and security.
- Identify missing tests and edge cases.
- Run formatter, linter, build and tests where available.
- Produce a change note and pull-request description with tests, risks and rollback considerations.

## 5. Constraints and non-goals

- Use a sandbox repository and synthetic data.
- Do not connect to production databases, secrets or customer systems.
- Do not allow an agent to merge or deploy code.
- Do not accept generated code without human review and actual test execution.
- Do not silently change public API contracts or database schemas.
- Keep changes small enough to inspect.

## 6. Claude services available

Choose a combination; do not force every service into the solution.

- **Claude AI (chat):** clarify requirements, compare designs, draft acceptance criteria and review plans.
- **Claude Code:** inspect the repository, edit code, run tests, review diffs and use project instructions, skills or subagents.
- **Claude Cowork:** work across selected design documents, issue descriptions and architecture notes; prepare supporting reports and handover artefacts.
- **Anthropic SDK / Claude API:** embed code explanation, change-impact Q&A or structured review assistance in an internal developer portal.
- **Claude Agent SDK:** build a controlled multi-step engineering agent using approved tools and bounded permissions.

In this pack, `claude_agent_framework` means the **Claude Agent SDK**, unless your training environment defines a different framework.

## 7. Decisions your team must make

1. Which tasks belong in Claude Code versus a custom application using the Anthropic SDK?
2. What repository context should be provided or excluded?
3. Which actions can be autonomous and which require developer approval?
4. How will the workflow prove that a claimed test actually ran?
5. How will it avoid inventing file paths, APIs or business rules?
6. What happens when requirements conflict or evidence is insufficient?
7. What quality gates must pass before a pull request is ready?

## 8. Exercise stages

1. **Frame:** define personas, requirements, acceptance criteria, constraints and non-goals.
2. **Explore:** map code and dependencies; verify findings against the repository.
3. **Plan:** create a change-impact report before editing.
4. **Build:** implement a narrow feature slice.
5. **Validate:** run tests, inspect diffs and challenge generated output.
6. **Govern:** define permissions, approvals, data boundaries and evidence.
7. **Present:** demonstrate the workflow and implemented change.

## 9. Acceptance criteria

- A developer can identify affected services and files with evidence.
- The implementation plan identifies assumptions and risks.
- Partial fulfilment is implemented for the agreed scope.
- Existing full-fulfilment behaviour remains covered.
- Tests cover full, partial and zero availability, duplicate requests and failure paths.
- The diff is reviewable and contains no unrelated changes.
- Actual test output is shown.
- No commit, merge or deployment occurs without explicit approval.
- Documentation matches the implementation.

## 10. Presentation

Prepare a 7–10 minute demonstration: codebase discovery; impact analysis; implementation plan; code change and test execution; one AI-assisted correction; service selection; approval points and production gaps.

## 11. Discussion questions

- How do you stop an agent making a broad refactor when only one feature is required?
- What is the source of truth when code and documentation disagree?
- How do you ensure generated tests are meaningful rather than merely matching the implementation?
- Which repository operations always require human approval?
- How will you measure productivity without reducing quality?
