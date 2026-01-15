# AI Multi-Agent System – Documentation Management System Project

## Project Information
- The project is available (public) in my personal GitHub repository:
- https://github.com/wagnersbfilho/langflow-multi-agent-project-management

## Project Overview
This repository contains a multi-agent AI system designed to support the planning, risk assessment, and delivery of a Documentation Management System (DMS).

The solution uses Langflow with OpenAI gpt-5 to orchestrate sequential AI agents, each aligned with PMBOK project management knowledge areas.

The project was developed for academic evaluation, focusing on structured project planning, risk management, and software delivery best practices.

The Langflow Installation Guide (Windows with WSL – Ubuntu) is described in **HELP.md**.

---

## Project Objectives
- Develop a complete Waterfall-based project plan
- Create a Work Breakdown Structure (WBS) with cost estimation
- Perform a comprehensive risk assessment
- Deliver a multi-agent AI solution with reproducible outputs

---

## Multi-Agent Architecture
The system is composed of seven sequential AI agents, where each agent consumes the structured output of the previous one.

- **Agent 1** → Scope & Requirements Analyst  
- **Agent 2** → Waterfall Project Planning Agent  
- **Agent 3** → WBS & Cost Estimation Agent  
- **Agent 4** → Risk Management Agent  
- **Agent 5** → Documentation & Consolidation Agent – Project Plan  
- **Agent 6** → Documentation & Consolidation Agent – WBS  
- **Agent 7** → Documentation & Consolidation Agent – Risk Assessment  

Each agent follows PMBOK best practices and performs a single, well-defined responsibility.

---

## Agent Responsibilities

### Agent 1 – Scope & Requirements Analyst
- Analyzes project scope and objectives  
- Identifies stakeholders, assumptions, and constraints  
- Produces structured functional and non-functional requirements  

### Agent 2 – Project Planning (Waterfall)
- Defines project phases  
- Estimates timelines and dependencies  
- Produces a textual Gantt chart  
- The **Deliverable 1 - Project Plan Development (Waterfall Methodology)** is generate after this agent

### Agent 3 – WBS & Cost Estimation
- Creates a three-level Work Breakdown Structure  
- Assigns roles and responsibilities  
- Estimates total project cost
- The **Deliverable 2 – Work Breakdown Structure (WBS)** is generate after this agent

### Agent 4 – Risk Management
- Identifies at least 15 categorized risks  
- Assesses likelihood and impact  
- Proposes mitigation strategies  
- Builds a risk prioritization matrix  
- The **Deliverable 3 – Risk Assessment** is generate after this agent

---

## Technology Stack
- **LLM:** OpenAI gpt-5  
- **Orchestration:** Langflow  
- **Methodology:** Waterfall (PMBOK-aligned)  
- **Output:** Markdown documentation and structured tables  

---

## How to Run the Project (Langflow)
1. Create a new flow in Langflow  
2. Import the Langflow JSON file  
3. Use the provided prompts for each agent  
4. If using an OpenAI model, set the API key  
5. Run the flow starting from Agent 1  

---

## Notes
- The project strictly follows PMBOK principles  
- Outputs are deterministic when configured properly  
- The system demonstrates AI-driven project management support  


## Respository Structure
│ \
├── input-prompts/ \
│   ├── agent1_business_analist.md \
│   ├── agent2_waterfall_project_planning.md \
│   ├── agent3_wbs_cost_estimation.md \
│   ├── agent4_risk_management.md \
│   ├── agent5_documentation_project_plan.md \
│   ├── agent6_documentation_wbs.md \
│   ├── agent7_documentation_risk_assessment.md \
│ \
├── langflow/ \
│   └── multi_agent_project_management_gpt_5.json \
│ \
├── outputs/ \
│   ├── project_plan.md \
│   ├── project_plan.pdf \
│   ├── risk_assessment.md \
│   ├── risk_assessment.pdf \
│   ├── wbs_cost.md \
│   ├── wbs_cost.pdf \
│ \
└── README.md \
└── HELP.md
