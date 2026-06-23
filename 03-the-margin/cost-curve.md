# Cost Curve & Pricing Strategy

## Cost Model

### Assumptions

Enterprise Profile (Modeled after a company like eBay)

* 12,000 employees
* 2,000 potential submitters
* 1,500 AI opportunities per year
* 750 opportunities reach governance review
* 250 pilots launched annually

### Cost Per Opportunity

| Cost Category        | Per Opportunity | Notes                                                |
| -------------------- | --------------- | ---------------------------------------------------- |
| Inference (Triage)   | $0.25           | Opportunity summarization, classification, routing   |
| Inference (Frontier) | $0.75           | Responsibility Design and governance recommendations |
| Infrastructure       | $0.50           | Workflow orchestration, dashboards, notifications    |
| Data / Storage       | $0.10           | Opportunity records and governance history           |
| Human-in-the-Loop    | $125            | PM review, AI PM review, governance committee review |
| **Total COGS**       | **~$126**       | Human review remains the dominant cost driver        |

### Current-State Cost

Manual governance process:

* Intake review
* Classification
* Risk assessment
* Governance meeting preparation
* Follow-up coordination

Estimated cost:

**$406 per opportunity**

### AI-Enabled Cost

Structured workflow plus AI assistance:

**$126 per opportunity**

### Cost Reduction

**69% reduction in governance cost per opportunity**

---

## Cascading Strategy

### Triage Model

GPT-4o Mini

Used for:

* Opportunity intake summarization
* Work classification recommendations
* Portfolio reporting
* Routing recommendations

### Frontier Model

GPT-5.5

Used for:

* Responsibility Design
* Autonomy recommendations
* Governance rationale generation
* High-risk opportunity reviews

### Routing Rule

Escalate to frontier model when:

* Risk Level = High
* Recommended Path = AI Agent
* Decision Criticality = High
* Human Judgment Required = High

All other opportunities remain on GPT-4o Mini.

### Expected Cascade Ratio

20:1

Approximately 95% of opportunities remain on the lower-cost model.

---

## Pricing Model

### Current Pricing

Most organizations today manage AI opportunities through:

* Email
* Spreadsheets
* Jira tickets
* Governance meetings

Effective software spend:

**$0**

Governance labor spend:

**$300K–$600K annually**

### Proposed AI Pricing

#### Enterprise

$250,000/year

Includes:

* AI Opportunity Management
* Governance Workflows
* Portfolio Reporting
* Review Dashboards

#### Enterprise Plus

$500,000/year

Includes:

* Governance Intelligence
* Advanced Reporting
* Pilot Tracking
* Portfolio Analytics

### Model

Hybrid

* Base Platform Fee
* Opportunity Volume Included
* Optional Premium Governance Analytics

Customers purchase governance capacity rather than AI tokens.

---

## Stress Tests

| Scenario                         | Impact on Margin | Response                                          |
| -------------------------------- | ---------------- | ------------------------------------------------- |
| Inference costs 3x               | Minimal (<3%)    | Human review remains primary cost driver          |
| Opportunity volume doubles       | Positive         | Fixed platform costs spread across larger volume  |
| Model provider raises prices 50% | Minimal          | Increase routing efficiency or shift providers    |
| Governance review time doubles   | Significant      | Improve workflow automation and review tooling    |
| Approval rates decline           | Moderate         | Improve classification and recommendation quality |
| AI recommendations lose trust    | Severe           | Increase transparency and human oversight         |

---

## Board One-Pager

### Before (Traditional Governance)

Revenue Driver

* None (internal process)

Economics

* Manual reviews
* Meeting-heavy process
* Spreadsheet tracking

Key Metrics

* Opportunities Reviewed
* Time to Decision
* Governance Labor Cost

Cost Per Opportunity

$406

Cycle Time

30 Days

---

### After (AI-Enabled Governance Platform)

Revenue Driver

* Enterprise Subscription
* Governance Intelligence
* Portfolio Analytics

Economics

* AI-assisted reviews
* Structured workflows
* Portfolio visibility

Key Metrics

* Cost Per Opportunity
* Approval Cycle Time
* Opportunities Governed Per Reviewer
* Pilot Success Rate

Cost Per Opportunity

$126

Cycle Time

7 Days

---

### Net Margin Shift

Traditional SaaS

Revenue = Seats

Cost = Infrastructure

Margin = High

AI Governance Platform

Revenue = Platform + Governance Intelligence

Cost = Human Review + Inference

Margin = Slightly Lower

Value Delivered = Significantly Higher

---

## Board Metric

### North Star Metric

Governance Cost Per Approved AI Opportunity

Before: $406

After: $126

Reduction: 69%

This metric captures throughput, efficiency, governance effectiveness, and business value in a single measure.
