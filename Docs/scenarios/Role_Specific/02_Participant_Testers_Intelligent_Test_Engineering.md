# Ness AI Engineering Challenge 02 — Test Engineers
## Intelligent Test Automation & Quality Intelligence

**Role:** Ness quality engineering team | **Team size:** 3–5 | **Duration:** 3–4 hours

> Fictional training scenario. Use synthetic requirements, test data and non-production environments only.

## 1. Business context

Ness provides quality engineering for a retail banking application covering onboarding, account servicing, payments and transaction history.

Requirements arrive as Jira stories, acceptance criteria, API specifications, UI mock-ups and change notes. Test engineers manually convert them into scenarios and automation scripts.

Problems include incomplete requirement-to-test traceability, missed negative and boundary scenarios, duplicate regression tests, brittle UI automation and lengthy failure triage across logs, screenshots and API responses.

## 2. Trigger event

A release passed regression but failed in production when a payment with a boundary-value amount was submitted for an unusual account state. The scenario was not covered because the acceptance criteria were interpreted too narrowly.

The team also spent hours distinguishing product defects from flaky automation and environment failures.

The client wants Ness to demonstrate AI-enabled quality engineering that improves traceability, coverage and failure diagnosis.

## 3. Your assignment

Build an **Intelligent Test Engineering Assistant** that takes a requirement or user story and helps QA move from requirements to validated test evidence.

## 4. Required capabilities

### Requirement analysis
- Accept a story, acceptance criteria or API specification.
- Identify rules, preconditions and dependencies.
- Detect ambiguity, missing criteria and conflicting statements.
- Generate clarification questions.
- Produce requirement-to-test traceability.

### Test design
- Generate positive, negative, boundary, equivalence-partition and state-transition scenarios where relevant.
- Identify risk-based scenarios.
- Include test data and expected outcomes.
- Detect duplicate/overlapping tests.
- Allow testers to edit and approve generated cases.

### Automation assistance
- Generate starter scripts for Playwright, Selenium, REST Assured or pytest.
- Reuse existing framework patterns and page objects.
- Generate API assertions and data-driven tests.
- Keep generated scripts separate from approved suites until reviewed.

### Failure intelligence
- Analyse synthetic test reports, stack traces, screenshot descriptions and API responses.
- Group similar failures.
- Classify likely product defect, environment, test-data, automation defect or flaky candidate.
- Provide evidence, uncertainty and next diagnostic steps.

### Quality dashboard
- Show requirements, generated/approved tests and execution results.
- Show coverage by requirement and risk.
- Highlight uncovered high-risk requirements.
- Export test and defect-triage summaries.

## 5. Constraints and non-goals

- Use synthetic requirements, results and data.
- Do not connect to production banking systems or use customer information.
- Do not automatically close defects or change release status.
- Generated tests are not approved until reviewed.
- Do not claim coverage based only on test-case volume.
- Do not invent execution results.
- Do not automatically run tests against production.

## 6. Claude services available

- **Claude AI:** analyse requirements, brainstorm edge cases and challenge test assumptions.
- **Claude Code:** inspect the automation repository, generate/update scripts, run tests and review diffs.
- **Claude Cowork:** analyse selected requirement folders and test reports; prepare traceability workbooks and release summaries.
- **Anthropic SDK / Claude API:** integrate structured test generation and failure classification into a QA portal.
- **Claude Agent SDK:** coordinate requirement analysis, test design, automation assistance and triage through approved tools and human review.

In this pack, `claude_agent_framework` means the **Claude Agent SDK**, unless your training environment defines a different framework.

## 7. Decisions your team must make

1. Which activities are suitable for AI generation and which need tester judgment?
2. How will each test map to a requirement?
3. How will you prevent invented execution results?
4. What evidence is needed before classifying a failure as a product defect?
5. How will flaky tests be distinguished from intermittent product defects?
6. Which automation changes require code review?
7. How will you measure quality rather than test volume?

## 8. Exercise stages

1. **Frame:** select a requirement and define the QA workflow.
2. **Analyse:** identify rules, ambiguity and risks.
3. **Design:** generate test scenarios and traceability.
4. **Automate:** generate and execute a small set of scripts.
5. **Triage:** analyse synthetic failures with evidence.
6. **Evaluate:** compare AI output with tester-reviewed expected results.
7. **Govern:** define approval, evidence, data and release boundaries.
8. **Present:** demonstrate the workflow end to end.

## 9. Acceptance criteria

- Ambiguity is detected and useful clarification questions are raised.
- Positive, negative and boundary scenarios are included.
- Each test maps to a requirement or is labelled exploratory.
- Automation follows the selected framework conventions.
- Execution status comes from actual runner output.
- Failure classification includes evidence and uncertainty.
- Generated, reviewed, approved and executed states are distinct.
- High-risk uncovered requirements are visible.
- Human approval remains part of test-suite and release decisions.

## 10. Presentation

Prepare a 7–10 minute demonstration: submit a requirement; show ambiguity detection; generate and review tests; generate and execute one automation script; analyse a synthetic failure; show traceability and coverage; explain governance.

## 11. Discussion questions

- Can AI-generated tests expose a requirement defect or simply repeat its ambiguity?
- How do you distinguish test coverage from meaningful risk coverage?
- What evidence is required to call a test flaky?
- How can AI help maintain automation without masking UI defects?
- What should never be inferred from a log or screenshot alone?
