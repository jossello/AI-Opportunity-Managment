# Compounding System Design

## Feedback Loops

| Loop                      | Input                                                   | Output                                                 | Compounds? | Status  |
| ------------------------- | ------------------------------------------------------- | ------------------------------------------------------ | ---------- | ------- |
| Governance Decisions      | Approval outcomes, conditions, rejections               | Better future governance recommendations               | Y          | Active  |
| Portfolio Intelligence    | Opportunity records, pilot results, deployment outcomes | Improved opportunity evaluation and prioritization     | Y          | Active  |
| Risk Classification       | PM and AI PM review decisions                           | More accurate risk and autonomy recommendations        | Y          | Active  |
| Cross-Functional Learning | IT, Security, Legal, HR feedback                        | Standardized governance patterns and policies          | Y          | Active  |
| Pilot Outcomes            | Pilot success metrics and business outcomes             | Better future pilot selection and investment decisions | Y          | Missing |

### Broken Loop Identified by Partner

Pilot outcomes are not currently connected back to opportunity records.

The system captures governance decisions but does not consistently learn whether approved pilots delivered business value.

### Fix Plan

Add a Pilot Outcome Review stage that captures:

* Business results
* User adoption
* Risk incidents
* Governance exceptions
* Production deployment decisions

Connect outcomes back to:

* Classification patterns
* Risk recommendations
* Responsibility models
* Governance conditions

This creates a closed-loop learning system.

---

## Context Connectivity

### Current State

The platform captures context across:

* Product
* Customer Service
* Finance
* HR
* Supply Chain
* IT

Each opportunity includes:

* Business function
* Work type
* Risk profile
* Governance decisions
* Accountability structures

### Knowledge Flow

Opportunity Intake
→ Work Classification
→ Responsibility Design
→ Governance Review
→ Pilot Tracking
→ Portfolio Intelligence

Knowledge becomes reusable through:

* Governance history
* Approval conditions
* Responsibility templates
* Risk patterns
* Pilot outcomes

### Potential Silos

* Department-specific workflows
* Local AI experiments
* Shadow AI tools
* Pilot outcomes tracked outside the system

Primary risk:

Organizations govern opportunities centrally but measure results locally.

---

## Governance Policy

### Scope

All AI opportunities involving:

* Employee-facing AI
* Customer-facing AI
* Process automation
* Decision support
* Decision execution
* Autonomous agents

### Autonomy Boundaries

Allowed Without Governance Review:

* Draft generation
* Content summarization
* Information retrieval

Requires Governance Review:

* Recommendations
* Automated workflows
* Customer-facing interactions
* Human resource decisions
* Financial decisions

Prohibited Without Executive Approval:

* Autonomous financial actions
* Employee performance decisions
* Legal commitments
* Customer-impacting decisions without oversight

### Escalation Triggers

* High-risk classification
* Recommend / Decide / Act autonomy
* Customer impact
* Financial impact
* Legal impact
* Security impact
* Employee impact

### Audit Cadence

Monthly

* Opportunity review
* Governance queue review
* Pilot review

Quarterly

* Policy review
* Risk model review
* Reliability review

### Regulatory Exposure

Potentially impacted by:

* EU AI Act
* GDPR
* State privacy regulations
* Employment regulations
* Consumer protection requirements

High-risk use cases require additional review and documentation.

---

## Agent Topology

### Intake Agent

Can:

* Summarize submissions
* Extract structured information
* Recommend classifications

Cannot:

* Approve opportunities
* Determine governance outcomes

---

### Classification Agent

Can:

* Recommend work types
* Recommend archetypes
* Recommend risk levels

Cannot:

* Override PM decisions

Human Approver:

Product Manager

---

### Responsibility Design Agent

Can:

* Recommend autonomy levels
* Recommend accountability structures
* Recommend governance paths

Cannot:

* Approve pilots
* Approve production deployment

Human Approver:

AI Product Manager

---

### Governance Assistant

Can:

* Generate review summaries
* Surface risks
* Recommend conditions

Cannot:

* Approve or reject opportunities

Human Approvers:

* IT
* Security
* Legal
* People & Culture

---

### Production Approval

Always Human

No AI agent can approve:

* Production deployment
* Governance exceptions
* Risk acceptance

---

## Shadow AI Audit

| Tool                       | Owner            | Risk Level | Decision |
| -------------------------- | ---------------- | ---------- | -------- |
| ChatGPT Enterprise         | Multiple Teams   | Medium     | Govern   |
| GitHub Copilot             | Engineering      | Medium     | Govern   |
| Marketing AI Content Tools | Marketing        | Low        | Keep     |
| Custom GPTs                | Individual Users | High       | Govern   |
| Autonomous Browser Agents  | Innovation Teams | High       | Govern   |

### Total Tools Found

25

### Tools After Triage

12

### Estimated Hidden Spend

$150,000 annually

Includes:

* Unapproved SaaS subscriptions
* Duplicate AI tooling
* Team-level experiments
* Department-specific licenses

---

## Strategic Insight

The primary compounding asset is not model performance.

It is organizational memory.

Every governance decision, approval condition, pilot outcome, accountability model, and risk assessment becomes part of an institutional knowledge system that improves future AI deployment decisions across the enterprise.

The platform becomes more valuable as the organization learns, even if the underlying models become commoditized.
