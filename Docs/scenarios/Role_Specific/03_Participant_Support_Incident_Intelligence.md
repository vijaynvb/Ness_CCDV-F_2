# Ness AI Engineering Challenge 03 — L1/L2 Support Engineers
## AI-Powered Incident Intelligence & Root Cause Analysis

**Role:** Ness application support team | **Team size:** 3–5 | **Duration:** 3–4 hours

> Fictional training scenario. Use synthetic logs, alerts, traces and runbooks only.

## 1. Business context

Ness provides L1/L2 support for a global e-commerce platform built with Java Spring Boot, .NET Core, Node.js, React, PostgreSQL, Redis and Kafka, deployed on Kubernetes.

L1 engineers review alerts and logs, perform initial diagnosis and escalate unresolved issues. During peak periods, several services generate large volumes of logs. One incident can create alerts in the API Gateway, order, payment and inventory services. Engineers investigate alerts separately and manually correlate timestamps and request identifiers.

## 2. Trigger event

During a recent sales event, customers reported failed or pending orders. Monitoring generated hundreds of alerts across multiple services. L1 opened separate tickets for symptoms later found to share a dependency failure.

It took 95 minutes to identify the likely source. The incident bridge lacked a consolidated timeline and the initial L2 escalation contained incomplete evidence.

The client wants an AI-powered support assistant that reduces investigation time while preserving safe operational controls.

## 3. Your assignment

Build an **Incident Intelligence & Root Cause Analysis Assistant** that helps L1/L2 engineers investigate incidents using logs, alerts, traces and approved runbooks.

## 4. Required capabilities

### Incident intake
- Accept an alert, ticket description or synthetic log bundle.
- Extract service, environment, timestamp, severity and correlation/request ID when available.
- Classify likely category: availability, latency, dependency, authentication, data, deployment or unknown.
- Identify missing diagnostic information.

### Log and event analysis
- Parse structured and unstructured samples.
- Group related errors by service, time window and correlation ID.
- Identify recurring error signatures.
- Build a chronological timeline.
- Distinguish observed facts from inferred hypotheses.

### Root cause assistance
- Generate ranked probable causes.
- Link hypotheses to log lines, metrics or trace evidence.
- Identify dependencies and downstream impact.
- Recommend diagnostic checks and approved runbook steps.
- State when evidence is insufficient and escalation is required.

### Knowledge and communication
- Search synthetic runbooks and known-error records.
- Show source document/section for recommendations.
- Identify stale or conflicting guidance.
- Prepare L1-to-L2 escalation, technical timeline, stakeholder update and post-incident review outline.

### Support dashboard
- Show incidents by severity and service.
- Group related alerts into suspected incidents.
- Show investigation status and next action.
- Record accepted, rejected or escalated recommendations.

## 5. Constraints and non-goals

- Use synthetic logs and sample runbooks.
- Do not connect to production observability platforms or execute production commands.
- Mask credentials, tokens, personal data and customer payloads.
- Do not restart services, scale clusters, delete data or change configurations.
- Do not present probable cause as confirmed root cause.
- Do not send stakeholder updates with unverified impact.
- Future remediation requires explicit authorisation, least privilege and approval.

## 6. Claude services available

- **Claude AI:** explain supplied log patterns, reason through hypotheses and draft communications.
- **Claude Code:** build parsers, normalisation utilities, dashboard and tests using synthetic data.
- **Claude Cowork:** analyse selected incident folders, ticket exports and runbooks; create timelines, handover packs and reports.
- **Anthropic SDK / Claude API:** integrate structured classification, summarisation and tool use into a support portal.
- **Claude Agent SDK:** implement a controlled multi-step support agent using approved read-only tools to retrieve runbooks, correlate evidence and prepare escalation recommendations.

In this pack, `claude_agent_framework` means the **Claude Agent SDK**, unless your training environment defines a different framework.

## 7. Decisions your team must make

1. Which log fields must be masked before model submission?
2. How will logs be correlated when request IDs are missing?
3. How will the assistant distinguish correlation from causation?
4. Which data sources and tools may the agent access?
5. Which operations must remain read-only?
6. What evidence threshold triggers escalation?
7. How will unsafe or outdated runbook recommendations be prevented?
8. What must be recorded for audit and incident review?

## 8. Exercise stages

1. **Frame:** define L1/L2 personas, incident workflow and scope.
2. **Ingest:** prepare synthetic logs, alerts and runbooks.
3. **Analyse:** build grouping, timeline and evidence extraction.
4. **Reason:** generate probable causes and recommended checks.
5. **Integrate:** use SDK/agent workflow to call approved read-only tools.
6. **Validate:** test known incidents, missing fields and conflicting evidence.
7. **Govern:** define masking, permissions, escalation and action boundaries.
8. **Present:** demonstrate incident intake through escalation.

## 9. Acceptance criteria

- Supplied log formats are parsed.
- Related alerts can be grouped into an incident hypothesis.
- A chronological timeline is generated.
- Findings distinguish facts, hypotheses and unknowns.
- Probable causes cite supporting evidence.
- Runbook recommendations show their source.
- Escalation includes impact, timeline, evidence and open questions.
- No production-changing action can be performed.
- Low-evidence cases are escalated.
- Sensitive fields are masked in the demo pipeline.

## 10. Presentation

Prepare a 7–10 minute demonstration: load a synthetic incident bundle; show grouping and timeline; review probable causes and evidence; retrieve a runbook; generate an L1-to-L2 escalation; explain read-only diagnosis versus remediation.

## 11. Discussion questions

- What if two services emit similar errors but only one is the source?
- What if timestamps use different time zones?
- What if a log bundle contains a secret or customer identifier?
- How do you prevent a dangerous command recommendation?
- What evidence is needed before declaring root cause?
- Which parts of incident response should remain human-led?
