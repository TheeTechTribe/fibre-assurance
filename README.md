# Predictive and Autonomous Fibre Network Assurance

An AI-enabled fibre network assurance solution designed to help network engineers detect network deterioration early, predict potential failures, assess service impact, prioritise risks, and investigate probable root causes before customers experience service disruption.

## Challenge

**Sponsor:** Openserve
**Domain:** AI-Enabled Intelligent Connectivity and Next-Generation Networks
**Challenge:** Predictive and Autonomous Fibre Network Assurance

Openserve aims to transform fibre network assurance from reactive fault management towards predictive and intelligent operations.

The challenge focuses on using network telemetry, alarms, historical incidents, topology, and operational data to:

* Detect network degradation early
* Predict potential network failures
* Identify probable root causes
* Assess potential customer and service impact
* Prioritise network risks
* Recommend appropriate corrective actions
* Improve operational responsiveness

## Our Concept

We propose an **AI-enabled Network Assurance Intelligence System** that continuously monitors fibre network health and assists engineers in identifying and investigating potential problems before they result in service disruption.

The solution follows a **human-in-the-loop approach**.

AI does not replace the network engineer or independently make operational decisions. Instead, it provides early detection, predictions, supporting evidence, risk information, and insights that enable engineers to make faster and better-informed decisions.

## Core Capabilities

### Real-Time Network Monitoring

Continuously analyse network telemetry and related operational information to understand the current health of the fibre network.

The system should distinguish between isolated fluctuations and meaningful patterns of deterioration to reduce unnecessary alerts.

### Anomaly Detection

Identify unusual network behaviour even when the behaviour does not correspond to a previously labelled fault.

Unknown anomalies can still be brought to an engineer's attention for investigation.

### Failure Prediction

Use historical incidents and network behaviour to estimate whether observed deterioration may result in network failure.

### Risk Assessment and Prioritisation

Detected risks are assessed and prioritised according to factors such as:

* Probability of failure
* Severity
* Time to potential disruption
* Number of customers affected
* Criticality of affected services

Critical services such as hospitals and emergency infrastructure should receive greater consideration when assessing service impact.

The final risk-scoring methodology will be determined through further research.

### Root-Cause Insights

Provide engineers with:

* The most likely cause of a detected problem
* Alternative possible causes
* Supporting factors contributing to the prediction
* Similar historical incidents where available

The objective is to reduce the amount of time engineers spend diagnosing network problems.

### Model Reliability

Predictions should be accompanied by information that helps engineers understand how much confidence they should place in the AI output.

This may include:

* Prediction confidence
* Historical model performance
* Relevant contributing factors
* Similar previous incidents

### Service Impact Assessment

Use network topology and service information to determine which customers and services could potentially be affected by a predicted network failure.

Impact should consider both the **number** and **criticality** of affected services.

### Proactive Customer Communication

Where potential disruption has been identified, the system can recommend that affected customers be notified before disruption occurs.

Customer communication remains subject to human approval.

### Engineer Feedback and Incident Documentation

Engineers can document how an incident was investigated and resolved using the organisation's required incident or resolution template.

Resolved incidents can contribute to the historical knowledge available to the system and support future model improvement.

### Operational Audit Trail

Maintain a timeline of significant events, for example:

```text
08:02  Deterioration pattern detected
08:07  Risk generated
08:10  Engineer notified
08:35  Alert acknowledged
09:10  Investigation initiated
10:25  Root cause confirmed
11:05  Issue resolved
```

This provides traceability and can support operational review and performance analysis.

## Proposed AI Approach

The project will investigate a combination of machine-learning techniques.

### Supervised Learning

Historical labelled incidents can be used to train models to recognise known degradation and failure patterns and predict future failures.

### Unsupervised Learning

Anomaly-detection techniques can identify network behaviour that differs significantly from normal operation, including behaviour that may not correspond to an existing labelled failure type.

Additional approaches will only be introduced where there is a demonstrated technical need.

## Proposed Intelligence Pipeline

```text
Network Telemetry, Alarms, Incidents & Topology
                    │
                    ▼
             Data Processing
                    │
                    ▼
           Anomaly Detection
                    │
                    ▼
       Deterioration Pattern Analysis
                    │
                    ▼
           Failure Prediction
                    │
                    ▼
        Probable Root-Cause Analysis
                    │
                    ▼
          Service Impact Analysis
                    │
                    ▼
             Risk Scoring
                    │
                    ▼
       Engineer Decision-Support Dashboard
                    │
                    ▼
        Incident Resolution & Feedback
```

## Dashboard Vision

The system should communicate its purpose immediately when an engineer opens it.

The primary dashboard should provide:

1. **Overall Network Health**
2. **Prioritised Risk Queue**
3. **Risk Severity and Service Impact**
4. **AI Diagnosis and Model Reliability**
5. **Real-Time Network Trends and Visualisation**

Engineers should only need to drill deeper when additional investigation is required.

## Research Areas

Before finalising the PoC architecture, the team will investigate:

* Fibre/PON network architecture
* Fibre network telemetry
* Common degradation and failure indicators
* Network alarms
* Optical performance measurements
* Anomaly-detection techniques
* Failure-prediction techniques
* Time-series deterioration detection
* Root-cause analysis
* Explainable AI
* Model reliability
* Network topology analysis
* Service-impact assessment
* Risk-scoring methodologies
* Alert fatigue
* Human-in-the-loop AI
* Operational audit trails

## Project Structure

```text
openserve-fibre-assurance/
│
├── docs/
│   ├── challenge/
│   ├── research/
│   ├── solution/
│   └── team/
│
├── data/
│   ├── raw/
│   ├── synthetic/
│   └── processed/
│
├── notebooks/
│
├── src/
│   ├── data/
│   ├── models/
│   ├── risk/
│   ├── explainability/
│   ├── services/
│   └── utils/
│
├── dashboard/
│
├── tests/
│
└── presentation/
```

## Current Project Phase

**Phase 1: Research and Solution Definition**

The team is currently validating the technical foundation of the proposed solution.

The first milestone will determine:

* What the system should predict
* Which network variables are realistically available
* What constitutes meaningful network deterioration
* Which failure scenarios should be represented in the PoC
* Which ML approaches are appropriate
* How model reliability will be evaluated
* How network risks should be scored
* How service impact should be calculated
* How engineers should interact with the system
* How resolved incidents can improve future predictions

## Team

This project is being developed by a team of three as part of the **SATNAC 2026 Industry Solutions Challenge**.

Team member responsibilities and research streams will be documented as the project progresses.

## Status

**Research and solution design in progress**

The architecture, datasets, machine-learning models, risk-scoring methodology, and implementation technologies remain subject to validation during the research and PoC development phases.
