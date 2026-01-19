# Deliverable 3 – Risk Assessment

## 1. Risk Register

| Risk ID | Risk Description | Category | Likelihood | Impact | Mitigation Strategy |
|--------|------------------|----------|------------|--------|---------------------|
| R1 | Real-time editing and document locking may cause conflicts/latency due to algorithmic complexity (4.1.5, 3.1.6) | Technical | Medium | High | Run early spike/prototype for OT/CRDT in 3.1.6; define acceptance/performance criteria in 2.1.4; implement conflict resolution and optimistic locking in 4.1.5; perform scalability tests in 6.1.4 and tune baselines in 5.1.10; monitor with dashboards in 5.1.9. |
| R2 | Third-party API limits/changes (S3/Drive/OneDrive, DocuSign/Adobe, PM tools) disrupt integrations (3.1.4, 4.1.9, 5.1.3) | Technical | Medium | High | Abstract integrations in 3.1.4; implement retries/backoff/caching in 4.1.9; validate SLAs and quotas in 5.1.3; add API health monitoring in 6.1.3 and 5.1.9; maintain vendor change watch and sandbox tests. |
| R3 | Search and indexing may not meet performance/scalability targets under peak loads (3.1.3, 6.1.4) | Technical | Medium | High | Optimize schema and indexes in 3.1.3; define KPIs in 2.1.7; run load/stress tests in 6.1.4; tune resources in 5.1.10; add performance monitoring/alerts in 3.1.10 and 5.1.9. |
| R4 | Sequential dependencies and large build scope (esp. 4.1.5 XL) cause schedule slippage | Project Management | High | High | Manage critical path and buffers from 1.1.6; break down 4.1.5 into increments; weekly schedule variance reviews; enforce phase gates and triage in 6.1.6; re-sequence non-critical tasks where possible. |
| R5 | Scope creep during requirements elaboration leads to rework and delays (2.1.1–2.1.8) | Project Management | Medium | High | Baseline SRS/RTM in 2.1.8; implement change control via governance from 1.1.3; prioritize with MoSCoW; tie acceptance criteria in 2.1.4; maintain risk/assumption log in 1.1.5. |
| R6 | Budget overrun from underestimated infra/licenses (15%) and integration effort | Project Management | Medium | Medium | Validate vendor quotes during 1.1.7 and 3.1.1; set contingency in 1.1.6; monitor burn vs plan weekly; enable cost monitoring tags/dashboards in 3.1.10; optimize architecture before 4.x commits. |
| R7 | Security Analyst bandwidth constraints across many security/compliance tasks (2.1.5, 3.1.5, 4.1.7, 5.1.4–5, 7.1.x) | Resource | Medium | High | Add backup security resource; schedule dedicated security sprints; outsource pentest (7.1.3) if needed; prioritize controls per 3.1.5; early booking for 7.1.1–7.1.7. |
| R8 | Integration Engineer as single point of failure for integrations/migrations (3.1.4, 4.1.9, 5.1.1, 5.1.3, 5.1.6–7, 10.1.2) | Resource | Medium | High | Cross-train backup engineer; pair programming and documentation in 3.1.4/4.1.9; stagger critical integration tasks; pre-build migration runbooks in 5.1.6–7. |
| R9 | DevOps overload during provisioning, monitoring, cutover, and hypercare (4.1.1, 3.1.7, 5.1.9–10, 10.1.x, 11.1.x) | Resource | Medium | Medium | Automate IaC in 4.1.16; pre-provision environments 4.1.1; finalize runbooks 8.1.5; augment with temporary DevOps for 10.x and 11.x; enforce change freeze during cutover. |
| R10 | Insufficient UAT participation from all personas may miss critical issues (8.1.2) | User Adoption | Medium | High | Secure stakeholder commitment in 1.1.2/1.1.3; schedule UAT windows early (8.1.1); provide clear scripts and acceptance criteria (8.1.1, 2.1.4); track completion and escalate via governance. |
| R11 | Training materials not tailored by role reduce adoption post go-live (9.1.1–9.1.3) | User Adoption | Medium | Medium | Build role-based curriculum (9.1.2); deliver targeted sessions (9.1.3); publish KB/quick-starts (9.1.4); gather feedback and iterate before 10.x. |
| R12 | Workflow/usability issues in collaboration and approvals create resistance (4.1.4, 5.1.2) | User Adoption | Medium | Medium | Prototype demos during 3.x/4.1.4; collect feedback in 2.1.1 workshops; adjust configurations in 5.1.2; include usability checks in UAT (8.1.2). |
| R13 | Data retention/privacy misconfiguration during migration breaches GDPR/HIPAA (5.1.4, 5.1.6–7, 7.1.5–6) | Compliance | Medium | High | Define policies in 2.1.5; enforce retention/watermarks in 5.1.4; run test migrations with verification; validate controls in 7.1.5–7.1.6; require sign-offs pre-10.1.2. |
| R14 | Incomplete audit logging and evidence package delays certification or audits (5.1.4, 7.1.7) | Compliance | Medium | Medium | Specify control/evidence checklist in 3.1.5; enable audit logs in 5.1.4; continuously collect evidence; perform internal audit dry-run before 7.1.7. |
| R15 | MFA/IP restriction gaps before go-live increase security risk (5.1.5, 7.1.4) | Compliance | Low | High | Enforce mandatory MFA/IP policies in 3.1.5; validate in 7.1.4; include go-live gate checks in 10.1.5; monitor post-go-live in 11.1.1. |

## 2. Risk Prioritization

| Risk ID | Priority Level |
|--------|----------------|
| R1 | High |
| R2 | High |
| R3 | High |
| R4 | High |
| R5 | High |
| R6 | Medium |
| R7 | High |
| R8 | High |
| R9 | Medium |
| R10 | High |
| R11 | Medium |
| R12 | Medium |
| R13 | High |
| R14 | Medium |
| R15 | Medium |