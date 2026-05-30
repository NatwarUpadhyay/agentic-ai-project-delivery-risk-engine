# Architecture

## Overview
The Agentic AI Project Delivery Risk Assessment Engine is a multi-agent system built in AWS PartyRock. It uses a dependency-aware orchestrator to route inputs through specialized agents that collaborate to produce risk analysis, mitigation guidance, and executive reporting.

## Core Components
- Input Layer: Project Description, Team Size, Planned Timeline
- Orchestrator: Dependency-aware routing and aggregation
- Agent Layer: Six specialized agents with clear responsibilities
- Output Layer: Structured widgets and executive report

## Agent Responsibilities
- Agent 1: Project Understanding
  - Classify project type, scope, stakeholders, and dependencies
  - Produce a business summary
- Agent 2: Risk Identification
  - Identify risks across scope, schedule, resource, technology, security, compliance, and stakeholder domains
- Agent 3: Probability and Impact
  - Assign probability and business impact scores
  - Provide reasoning for each risk score
- Agent 4: Mitigation Planning
  - Define mitigation actions, contingency plans, and preventive measures
- Agent 5: Resource and Timeline Assessment
  - Assess feasibility, capacity, and bottlenecks
- Agent 6: Executive Reporting
  - Synthesize a boardroom-ready report with recommendations

## Dependency Graph
```mermaid
graph TD
  A1[Project Understanding] --> A2[Risk Identification]
  A1 --> A5[Resource and Timeline]
  A2 --> A3[Probability and Impact]
  A3 --> A4[Mitigation Planning]
  A2 --> A6[Executive Reporting]
  A3 --> A6
  A4 --> A6
  A5 --> A6
```

## Parallel Execution
```mermaid
flowchart TB
  A1[Project Understanding] --> P{Parallel Workstreams}
  P --> A2[Risk Identification]
  P --> A5[Resource and Timeline]
  A2 --> A3[Probability and Impact]
  A3 --> A4[Mitigation Planning]
  A4 --> J[Join]
  A5 --> J
  J --> A6[Executive Reporting]
```

## Executive Report Pipeline
```mermaid
flowchart LR
  PS[Project Summary] --> ER[Executive Report]
  RR[Risk Register] --> ER
  HM[Risk Heat Map] --> ER
  MP[Mitigation Plan] --> ER
  RT[Resource and Timeline Assessment] --> ER
  ER --> OUT[Health Score and Recommendations]
```

## Output Widgets
- Project Summary
- Risk Register
- Risk Heat Map Summary
- Project Health Score
- Success Probability
- Mitigation Plan
- Executive Report
- Recommended Next Steps

## Design Principles
- Dependency-based execution
- Parallel task execution where safe and traceable
- Structured, audit-friendly outputs
- Professional tone aligned to project governance standards
