# Agentic AI Project Delivery Risk Assessment Engine

A professional, multi-agent risk assessment engine built in AWS PartyRock. This project demonstrates agentic AI principles through a structured, dependency-aware pipeline that helps delivery teams assess project risks before execution.

## Project Overview
This repository documents the Agentic AI Project Delivery Risk Assessment Engine, a multi-agent system for IT services companies, consulting firms, PMOs, delivery managers, AI teams, and project managers. The app accepts three inputs and produces a boardroom-ready risk assessment with mitigation guidance and an executive summary.

This is a learning example built with AWS PartyRock. PartyRock provides the primary app-building platform; this repo documents the architecture, outputs, and learnings.

**Inputs**
- Project Description
- Team Size
- Planned Timeline

**Key Outputs**
- Project Summary
- Risk Register
- Risk Heat Map Summary
- Project Health Score
- Success Probability
- Mitigation Plan
- Executive Report
- Recommended Next Steps

## Getting Started (AWS PartyRock)
1. Open the AWS PartyRock app link in the section below.
2. Enter the three inputs (Project Description, Team Size, Planned Timeline).
3. Review the output widgets and executive report.

**Sample Input**
- Project Description: Enterprise GenAI platform for a banking client with RAG, document intelligence, chatbot UX, RBAC, Azure OpenAI integration, and CRM integration.
- Team Size: 6
- Planned Timeline: 4 months

**What You Will Receive**
- Structured risk register with probability and impact scoring
- Risk heat map summary and project health score
- Mitigation plan with preventive and contingency actions
- Executive summary with recommendations and immediate actions

## Business Problem
Project delivery teams often commit to aggressive timelines and broad scopes without a structured, pre-execution risk assessment. This leads to avoidable delays, budget overruns, compliance gaps, and stakeholder misalignment. The goal of this system is to surface delivery risks early, quantify impact, and provide actionable mitigation strategies before execution begins.

## Why Agentic AI
- Decomposes complex delivery risk analysis into specialized, expert roles
- Enables parallel workstreams with dependency-aware orchestration
- Improves traceability and auditability of risk decisions
- Produces consistent, structured outputs for governance and executive review

## Architecture Diagram (Mermaid)
```mermaid
flowchart LR
  I1[Project Description] --> O[Orchestrator]
  I2[Team Size] --> O
  I3[Planned Timeline] --> O

  O --> A1[Agent 1: Project Understanding]
  A1 --> A2[Agent 2: Risk Identification]
  A2 --> A3[Agent 3: Probability and Impact]
  A3 --> A4[Agent 4: Mitigation Planning]
  A1 --> A5[Agent 5: Resource and Timeline Assessment]

  A2 --> A6[Agent 6: Executive Reporting]
  A3 --> A6
  A4 --> A6
  A5 --> A6

  A6 --> OUT[Output Widgets]
```

## Agent Workflow
**Agent Responsibilities**
- Agent 1: Project Understanding Agent
  - Analyze project scope
  - Identify complexity, stakeholders, and dependencies
  - Generate a business summary
- Agent 2: Risk Identification Agent
  - Identify scope, schedule, resource, technology, security, compliance, and stakeholder risks
  - Categorize risks by severity
- Agent 3: Probability and Impact Agent
  - Assign probability and business impact
  - Provide reasoning for scoring
- Agent 4: Mitigation Planning Agent
  - Generate mitigation actions and contingency plans
  - Recommend preventive measures
- Agent 5: Resource and Timeline Assessment Agent
  - Evaluate feasibility of team size and timeline
  - Detect bottlenecks and capacity gaps
- Agent 6: Executive Reporting Agent
  - Produce executive summary, health score, success probability, and recommendations

**Agent Dependency Graph (Mermaid)**
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

**Parallel Execution Flow (Mermaid)**
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

**Executive Report Generation Pipeline (Mermaid)**
```mermaid
flowchart LR
  PS[Project Summary] --> ER[Executive Report]
  RR[Risk Register] --> ER
  HM[Risk Heat Map] --> ER
  MP[Mitigation Plan] --> ER
  RT[Resource and Timeline Assessment] --> ER
  ER --> OUT[Health Score and Recommendations]
```

## Screenshots
![Screenshot 1](assets/images/screenshot-01.png)
Input form for project description, team size, and planned timeline.
![Screenshot 2](assets/images/screenshot-02.png)
Agent workflow and widget dependency visualization in PartyRock.
![Screenshot 3](assets/images/screenshot-03.png)
Project understanding report generated by the Project Understanding Agent.
![Screenshot 4](assets/images/screenshot-04.png)
Executive report widget synthesizing results into a boardroom-ready summary.
![Screenshot 5](assets/images/screenshot-05.png)
AWS AI and ML Scholars challenge completion badge.

## Project Structure
- assets/images: UI screenshots used in this README
- assets/certificates: Certificate and credentials
- assets/source: Source materials referenced in documentation
- docs: Architecture and usage documentation

## Results (Sample)
Example outcomes from a regulated banking GenAI platform case study:
- 30-item risk register across scope, schedule, resource, technology, security, compliance, and stakeholder categories
- Project health score: 15/100 (critical)
- Success probability: 18%
- Clear executive recommendations and immediate action items for Weeks 1 to 2

## Future Improvements
- Monte Carlo delivery simulations and cost variance modeling
- Integration with Jira, Azure DevOps, and ServiceNow for risk tracking
- Exportable risk register to CSV and PDF
- Customizable risk taxonomies by industry and region
- Role-based governance dashboards

## Learning Outcomes
- Designing dependency-aware agent orchestration
- Applying structured risk management frameworks with AI
- Producing executive-grade reporting from agent outputs
- Balancing parallel execution with accountability and traceability

## AWS PartyRock Link
AWS PartyRock App: https://partyrock.aws/u/your-handle/your-app

## Certificate
Udacity Certificate: [assets/certificates/udacity-certificate.pdf](assets/certificates/udacity-certificate.pdf)

## Source Materials
Project Document: [assets/source/project-delivery-risk-assessment-engine.docx](assets/source/project-delivery-risk-assessment-engine.docx)

## Documentation
- [docs/architecture.md](docs/architecture.md)
- [docs/how-it-works.md](docs/how-it-works.md)
- [docs/use-cases.md](docs/use-cases.md)
- [docs/future-enhancements.md](docs/future-enhancements.md)

## Author
Natwar Upadhyay

## License
MIT. See [LICENSE](LICENSE).
