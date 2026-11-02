# Risk Register: Urban Tempo Smart Fleet & Transit

**Project Name:** Urban Tempo Smart Fleet & Transit  
**Project Manager:** Benjamin Ferguson  
**Project Sponsor:** Katherine Kopp  
**Target Launch Date:** 2026-11-20  
**Repository:** https://github.com/Urban-Tempo-Team/Urban-Tempo-and-Smart-Fleet  
**Date Created:** 2026-11-02  
**Last Updated:** 2026-11-02

## Purpose of This Document

Urban Tempo runs 350 buses and service vehicles using spreadsheets and post-failure maintenance logs. Our project builds an IoT Telemetry & Predictive Maintenance Platform that reads live vehicle data, predicts faults, creates work orders and feeds route delays to transit apps. This register tracks what could stop us from delivering that, and is reviewed every week.

## Risk Scoring

Score = Probability (1-3) × Impact (1-3)

| Score | Priority |
|-------|----------|
| 7-9 | Critical: immediate attention |
| 5-6 | High: actively manage |
| 3-4 | Medium: monitor |
| 1-2 | Low: watchlist |

## Risk Register Table

| ID | Risk Description | Category | Probability (1-3) | Impact (1-3) | Risk Score | Response Strategy | Mitigation Plan | Owner | Status | Last Update |
|----|-----------------|----------|-------------------|--------------|------------|-------------------|-----------------|-------|--------|------------|
| R-01 | Nov 20, 2026 launch is too tight for a 350-vehicle IoT platform; the repo has only planning documents so far | Schedule | 3 (High) | 3 (High) | 9 | Avoid | Launch as a pilot (one depot, 3 core features); set milestone dates; get sponsor approval for a phased rollout | Project Manager | Active | 2026-11-02 |
| R-02 | Not enough historical data to train accurate failure predictions (only spreadsheets and post-failure logs) | Technical | 3 (High) | 3 (High) | 9 | Mitigate | Start with rule-based alerts; clean old maintenance logs; train first model on a pilot group | Systems Architect | Active | 2026-11-02 |
| R-03 | Sensors may not work across a mixed fleet of buses and service vehicles | Technical | 2 (Medium) | 3 (High) | 6 | Mitigate | List fleet by make and model; pilot hardware on each vehicle type; keep manual entry as backup | Systems Architect | Active | 2026-11-02 |
| R-04 | Wrong predictions create false work orders or miss real faults; no test plan yet | Quality | 2 (Medium) | 3 (High) | 6 | Mitigate | Write test plan and acceptance criteria early; test with simulated data; technician approves work orders in pilot | QA & Testing Lead | Active | 2026-11-02 |
| R-05 | Integration with maintenance shops and transit apps is harder than estimated | Technical | 2 (Medium) | 3 (High) | 6 | Mitigate | Define interfaces early; confirm shop workflow; test with mock data first | Systems Architect | Active | 2026-11-02 |
| R-06 | Transit Director requested a passenger-crowding feature; no decision recorded | Scope | 2 (Medium) | 3 (High) | 6 | Control | Record the decision in the change board log; move to Phase 2 backlog; re-plan if approved | Lead Business Analyst | Active | 2026-11-02 |
| R-07 | Team lacks data science, IoT and security skills | Resource | 3 (High) | 2 (Medium) | 6 | Mitigate | Use managed cloud IoT and ML services; ask sponsor for part-time experts; cross-train backups | Project Manager | Active | 2026-11-02 |
| R-08 | Staff used to spreadsheets may not adopt the system; no training owner in the RACI | Stakeholder | 3 (High) | 2 (Medium) | 6 | Mitigate | Assign a training owner; role-based guides; one champion per depot; run old process in parallel | Lead Business Analyst | Active | 2026-11-02 |
| R-09 | Budget is not defined; hardware for 350 vehicles could exceed funding | Financial | 2 (Medium) | 3 (High) | 6 | Mitigate | Build cost estimate with 10-15% buffer; buy hardware in phases; prepare pilot-only plan | Project Manager | Active | 2026-11-02 |
| R-10 | Vehicle and GPS data could be hacked or misused (security and privacy) | External | 2 (Medium) | 3 (High) | 6 | Mitigate | Encrypt data; control access; set data-retention policy; security review before pilot | Systems Architect | Active | 2026-11-02 |

## Risks Identified

| Epic | Related Risks |
|------|---------------|
| Engine Diagnostics | R-02, R-03, R-04 |
| Maintenance | R-04, R-05 |
| Routing | R-05, R-06 |
| Training | R-08 |
| Whole project | R-01, R-07, R-09, R-10 |

## Owners

| Role | Person | Owns |
|------|--------|------|
| Project Manager | Benjamin Ferguson | R-01, R-07, R-09 |
| Systems Architect | Andrew Hendrickson | R-02, R-03, R-05, R-10 |
| Lead Business Analyst | Charles Jaramillo | R-06, R-08 |
| QA & Testing Lead | Jack Kanis | R-04 |

## Response Strategies Used

- **Avoid**: Shrink the Nov 20 launch to a pilot (R-01)
- **Mitigate**: Rule-based alerts, pilot hardware tests, test plan, cloud services (R-02 to R-05, R-07 to R-10)
- **Control**: Change control board log for the crowding feature request (R-06)

## Weekly Risk Review Questions

1. Is the Nov 20 pilot scope still achievable, and is Sprint 2 on track?
2. Has the Transit Director or sponsor decided on the passenger-crowding feature?
3. Do we have enough sensor data to test the predictions yet?
4. Are the Kanban limits (WIP 4, QA 2) being hit, and is QA a bottleneck?
5. Is anyone still without training or a named owner?
6. Have new risks come from the GitHub issues or the project board?
