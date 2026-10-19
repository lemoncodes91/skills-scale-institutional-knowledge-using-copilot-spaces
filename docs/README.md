# OctoAcme Project Management Docs

This README centralizes OctoAcme's project management process documents, gives a short summary of our approach, and provides direct links to the full documents in the docs/ folder.

## Brief overview of OctoAcme project management processes

OctoAcme uses a customer-first, iterative delivery approach with clear role assignments and lightweight artifacts to ensure teams deliver measurable value. Work begins with a Project One‑pager (problem, objectives, success metrics, stakeholders, and a high‑level timeline) that gates whether an initiative moves into planning. Planning breaks approved initiatives into shippable backlog items, defines a Definition of Done, estimates scope, and produces a release plan with milestones.

During execution, teams follow a regular cadence: brief daily standups for progress and blockers, weekly delivery syncs to align on progress and risks, and demos/reviews at the end of each sprint or milestone. Project boards (Backlog → Ready → In Progress → In Review → QA → Done) make status and cross-team dependencies visible. Pull requests are kept small, include acceptance criteria and issue links, and require automated CI checks and at least one approval before merging.

Quality and release controls are integral: unit, integration, and smoke tests are required where applicable, security scanning runs in CI, and manual QA is used for acceptance as needed. Releases are classified (patch/minor/major) and require pre‑release checks (passing CI & security scans, release notes, rollback plan, and smoke tests); post‑deploy verifications and an incident playbook ensure rapid response and learning.

Retrospectives after sprints, releases, or incidents capture learnings and convert them into prioritized action items tracked in the backlog. A maintained risk register, clear escalation paths (team → PM → Product Lead → Sponsor), and regular stakeholder updates preserve transparency and enable timely intervention.

## Documents

- [Project Management Overview](octoacme-project-management-overview.md)
- [Project Initiation Guide](octoacme-project-initiation.md)
- [Project Planning](octoacme-project-planning.md)
- [Execution & Tracking](octoacme-execution-and-tracking.md)
- [Release & Deployment Guide](octoacme-release-and-deployment.md)
- [Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md)
- [Risk Management & Communication](octoacme-risks-and-communication.md)
- [Roles & Personas](octoacme-roles-and-personas.md)

## How to use

- Link this README from the repo root or main project README for quick access.
- Keep the Project One‑pager and process-specific docs updated in the project repo (docs/ or .copilot/) so Copilot Spaces and contributors can use them as context.
- When adding new process documents, update this file to include a link.
