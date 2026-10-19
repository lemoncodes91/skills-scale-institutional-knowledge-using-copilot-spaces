# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

---

## Additional Suggested Personas (New)

The following personas are proposed to fill cross-cutting gaps in ownership, reduce single-person dependencies, and clarify interfaces between product, engineering, operations, and customer-facing teams.

### Release Manager

Role summary
- Coordinates and owns release planning and execution across teams to ensure releases are reliable, low-risk, and well-communicated.

Responsibilities
- Own release calendars, deployment windows, and release notes
- Maintain rollback / mitigation plans for releases
- Coordinate cross-team readiness (dev, QA, SRE, security, product ops)
- Lead release day activities and post-release verification

Decision authority
- Gatekeeper for non-emergency release approvals (can delay/cancel release if readiness criteria are unmet)
- Coordinate emergency releases with PM and SRE

Typical interactions
- Works with PM to align release scope with priorities
- Schedules with Developers and QA to ensure artifacts are ready
- Coordinates with SRE and Security for production checks
- Notifies Product Ops and Support for stakeholder readiness

When to escalate / handoffs
- Escalate to PM if release scope or timing conflicts with business priorities
- Handoff to SRE on-call for production verification once deployment completes

---

### Site Reliability Engineer (SRE) / Production Reliability Lead

Role summary
- Ensures service availability, performance, and operational readiness for production services.

Responsibilities
- Define and maintain runbooks, alerts, and SLOs
- Lead incident response and post-incident reviews
- Implement and review observability and on-call tooling
- Advise on capacity, reliability-related design, and deployment practices

Decision authority
- Can initiate rollbacks or mitigations for incidents in production
- Authorize changes that materially affect operational risk in consultation with Release Manager

Typical interactions
- Works closely with Developers to design for reliability and observability
- Coordinates with Release Manager on deployment impact and runbook readiness
- Escalates security or systemic issues to Security and PM as needed

When to escalate / handoffs
- Escalate to Product Lead for business-impacting reliability incidents
- Handoff incident follow-up actions to owners and track in the risk register

---

### UX Researcher / Design Lead (Research Lead)

Role summary
- Validates user needs, designs user experiences, and defines UX acceptance criteria to ensure usability and accessibility.

Responsibilities
- Run user research and usability tests
- Produce wireframes, mockups, and design specs
- Define UX acceptance criteria for features
- Validate accessibility and internationalization needs

Decision authority
- Advocate for design decisions and acceptance criteria; escalate scope trade-offs with the Product Manager

Typical interactions
- Partners with Product Manager to define user requirements
- Works with Developers and QA to ensure designs are implementable and testable
- Provides artifacts and acceptance criteria for PRs and sprint stories

When to escalate / handoffs
- Escalate to Product Manager when research findings require reprioritization
- Handoff validated designs and acceptance criteria before stories enter sprint

---

### Data Analyst / Measurement Lead

Role summary
- Owns success metrics definition, instrumentation guidance, and analysis to measure product outcomes.

Responsibilities
- Define key metrics and event schemas
- Review and validate instrumentation and telemetry
- Build dashboards and run analyses to assess feature impact
- Support A/B testing and experiment design

Decision authority
- Confirms metric validity and approves launch gating based on data readiness

Typical interactions
- Works with PM to align on success criteria
- Coordinates with Developers and SRE to ensure proper telemetry and event tracking
- Provides insights to Product, PM, and stakeholders for decision making

When to escalate / handoffs
- Escalate to Product Lead if metrics show unexpected or high-impact regressions
- Handoff dashboard ownership and runbooks for ongoing metric monitoring

---

### Security Engineer

Role summary
- Ensures security considerations are embedded throughout planning, development, and releases.

Responsibilities
- Conduct threat modeling and security reviews
- Triage vulnerabilities and coordinate remediation
- Define security acceptance criteria and scanning requirements
- Advise on compliance requirements and controls

Decision authority
- Can block releases if critical vulnerabilities or compliance gaps are detected
- Authorize security exceptions in conjunction with Product/Security leadership

Typical interactions
- Consults in planning for features with sensitive data or increased risk
- Works with Developers and SRE to fix vulnerabilities and harden systems
- Coordinates with Release Manager to ensure security checks are completed pre-release

When to escalate / handoffs
- Escalate critical findings to Security leadership and PM
- Handoff remediation ownership to engineering teams and track through to closure

---

### Product Operations / Business Analyst

Role summary
- Bridges product and business teams, owning release readiness for stakeholders, documentation, and training materials.

Responsibilities
- Prepare stakeholder communications and release announcements
- Maintain runbooks for business processes impacted by product changes
- Coordinate launch readiness with Sales, Support, and Marketing
- Produce end-user documentation and training material

Decision authority
- Can hold back stakeholder-facing communications until readiness checks pass
- Coordinate go/no-go for business readiness in collaboration with PM

Typical interactions
- Works with PM and Release Manager to time communications
- Interfaces with Customer Success, Sales, and Support to prepare for releases
- Ensures documentation and training resources are available pre-release

When to escalate / handoffs
- Escalate to PM for unresolved stakeholder readiness blockers
- Handoff to Support/CS prior to release for post-release monitoring and training

---

### Customer Success / Support Liaison

Role summary
- Represents customer needs and feedback, ensuring support readiness and closing the loop on customer-reported issues.

Responsibilities
- Communicate customer feedback and operational pain points to Product and Engineering
- Prepare support triage guidance for new releases
- Assist in validating that support processes and playbooks are updated
- Track and report post-release customer impact and issues

Decision authority
- Can request release delays if customer-impacting readiness or major regressions are identified

Typical interactions
- Works with Product Ops and PM to prioritize customer-facing issues
- Coordinates with Developers and SRE for triage on production issues
- Provides post-release reports to PM and stakeholders

When to escalate / handoffs
- Escalate major customer-impact incidents to PM and SRE
- Handoff support tickets and post-release feedback into product backlog

---

## Guidance for Adding Personas to Project Docs

- For each persona added to docs/octoacme-roles-and-personas.md include:
  - Short role summary
  - Key responsibilities (3–6 bullets)
  - Decision authority (what they can approve/block)
  - Typical interactions (who they coordinate with and when)
  - Examples of handoffs and escalation paths

- Keep persona entries concise and actionable. Link to role-specific runbooks (e.g., release runbook, incident runbook) where appropriate.

---
