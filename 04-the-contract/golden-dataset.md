# Golden Dataset & Reliability Contract

## Golden Dataset Spec

### Purpose

Validate whether the system correctly:

* Classifies work
* Identifies risk
* Recommends appropriate autonomy levels
* Routes opportunities to the correct governance path
* Escalates when required

| #  | Input Scenario                                             | Expected Output                                     | Edge Case? | Judge Type |
| -- | ---------------------------------------------------------- | --------------------------------------------------- | ---------- | ---------- |
| 1  | Customer service chatbot drafts responses for human review | Copilot, Draft Autonomy, Medium Risk                | N          | Rule       |
| 2  | AI automatically approves customer refunds up to $20       | Automation, Act Autonomy, Financial Risk Escalation | N          | Rule       |
| 3  | HR assistant recommends employee performance ratings       | Human Review Required, High Risk                    | Y          | Rule       |
| 4  | Marketing content generation for social media              | Creator Archetype, Draft Autonomy, Low Risk         | N          | Rule       |
| 5  | AI agent modifies pricing recommendations without approval | Escalate, High Risk, Governance Review Required     | Y          | Rule       |
| 6  | Finance forecasting assistant generating recommendations   | Oracle Archetype, Recommend Autonomy, High Risk     | Y          | LLM        |
| 7  | Internal knowledge search assistant                        | Information Retrieval, Low Risk                     | N          | Rule       |
| 8  | Autonomous vendor contract review and approval             | Reject or Escalate, Legal Risk                      | Y          | Rule       |
| 9  | Supply chain anomaly detection and monitoring              | Monitoring Archetype, Recommend Autonomy            | N          | LLM        |
| 10 | Customer support AI interacting with minors                | Escalate, High Risk, Additional Controls Required   | Y          | Rule       |

### Adversarial Rows Included

* Hidden decision authority
* Regulatory compliance scenarios
* Human accountability ambiguity
* Financial approval workflows
* Employee-impacting decisions
* Customer harm scenarios

### Coverage Gaps Identified

* Multi-agent workflows
* International regulatory requirements
* Cross-functional ownership disputes
* Human override failures
* Agent-to-agent coordination

---

## Confidence UX Design

### Approach

Confidence is never shown as a raw probability.

Instead, confidence determines workflow routing.

Users see:

* Recommendation
* Reasoning
* Required review level

### High Confidence (>90%)

Characteristics:

* Similar to previously approved opportunities
* Low risk
* Strong classification match

User Experience:

* Auto-populate recommendations
* Single reviewer approval

---

### Medium Confidence (70–90%)

Characteristics:

* Novel use case
* Mixed signals
* Moderate risk

User Experience:

* Recommendation plus rationale
* Human validation required

---

### Low Confidence (<70%)

Characteristics:

* Ambiguous problem statement
* Multiple possible classifications
* Missing information

User Experience:

* Escalation trigger
* Additional questions required
* AI recommendation withheld

---

### User Control Surface

Users can:

* Accept recommendation
* Modify recommendation
* Reject recommendation
* Escalate recommendation
* Flag recommendation for governance review

All actions become training and evaluation signals.

---

## Reliability Contract

| Metric                             | Target                    | Measurement                            | Alert Threshold  |
| ---------------------------------- | ------------------------- | -------------------------------------- | ---------------- |
| Classification Accuracy            | >95%                      | Agreement with PM review               | <90%             |
| Governance Recommendation Accuracy | >90%                      | Agreement with AI PM review            | <85%             |
| Hallucination Rate                 | <2%                       | Unsupported recommendations            | >5%              |
| Escalation Recall                  | >95%                      | High-risk cases correctly escalated    | <90%             |
| Latency (p95)                      | <5 seconds                | End-to-end recommendation generation   | >10 seconds      |
| Drift Velocity                     | <5% quarterly degradation | Golden dataset performance             | >10% degradation |
| Human Override Rate                | <20%                      | Recommendations significantly modified | >35%             |

---

## HITL Architecture

### Stage 1: Opportunity Intake

Human:

Submitter

AI:

Drafts classification recommendation

Escalation Trigger:

Missing or ambiguous information

---

### Stage 2: Work Classification

Human:

Product Manager

AI:

Suggests work type, archetype, risk level

Escalation Trigger:

High-risk classification

---

### Stage 3: Responsibility Design

Human:

AI Product Manager

AI:

Recommends autonomy level and governance model

Escalation Trigger:

Recommend or Decide autonomy

---

### Stage 4: Governance Review

Humans:

* IT
* Security
* Legal
* People & Culture

AI:

Provides recommendation and rationale

Escalation Trigger:

Any stakeholder rejection

---

### Stage 5: Pilot Approval

Human:

Governance Committee

AI:

Cannot approve pilots

Human approval required for all production deployment decisions.

---

## Red-Team Findings

### Most Likely Failure Mode

The system incorrectly classifies a high-risk opportunity as low-risk because the submitter describes the implementation rather than the actual business outcome.

Example:

"Generate refund recommendations"

Appears low-risk.

Actual workflow:

"Automatically approve refunds under $500."

The real risk is decision execution, not recommendation generation.

### Mitigation

Require the system to separately classify:

* Work Being Performed
* Decision Authority
* Business Impact
* Failure Consequences

before generating governance recommendations.
