# Non-functional requirements (NFRs) and risk-driven discovery
## Solve NFRs early, or pay a lot later
Delaying availability, performance, security and similar constraints forces redesigns (architecture, data, tech stack) and skyrockets costs; treat them first.

## Prioritize by future cost-of-change risk
Rank NFRs by “most expensive to change later” and start there to reduce uncertainty and technical debt.

## Think like an experimenter, not a fortune teller
Turn NFRs into spikes/validation experiments (e.g., heat tests at 45°C, response-time load tests) to learn fast and guide design.

## Hardware magnifies NFR risk
In hardware (molds, mass production), late changes are dramatically costly; prototype cheaply (3D printing, throwaway builds) and validate early.

## Avoid over- and under-design
Match design to context: overbuilding (e.g., finance-grade stack for a learning app) wastes money; underbuilding for mission-critical needs is risky.

## Measure what customers truly need
Quantify service levels (e.g., 99.99% availability for finance; less elsewhere) and how you’ll measure them (uptime, response SLAs) to set realistic targets.

---
# Backlog flow and slicing for clarity and focus
## Slice on “and” to reveal smaller value
date: 2025-09-11
If a backlog item combines multiple goals (“concepts and events”), split it so you can decide, deliver, and learn faster.

## Treat every PBI as a hypothesis
Features are bets; build to validate outcomes, not to “finish tasks.”

## Use a Product Board as a single source of truth
Visualize flow from New → Refinement → Product Backlog → Sprint → Done; include “Later” and “Won’t do” to increase transparency.

## Map to decide, not decorate
Use mapping techniques (journey mapping, risk maps, value slicing) to aid priority decisions, not to create artifacts for their own sake.

## Keep “Next focus” visible
Show current goals and what’s likely next to align stakeholders and preempt priority churn.

## Be ready to discard and rewrite cards
Refinement is a thinking process: it’s normal to throw away cards and replace them with better, smaller ones.

---
# Service work, defects, and DevOps within Sprints
## Separate “service lane” from planned delivery
Track production support/operations alongside sprint work (same board), so the team can make trade-offs explicitly.

## Bugs: feature-request or urgent defect?
- If it’s “by design” or an enhancement request → Product Backlog and prioritize.
- If it breaks existing behavior or blocks users → stop and fix in Sprint Backlog.

## Decide locally; don’t bottleneck the PO
Enable the team to triage and act on issues using agreed rules (SLA, severity) without waiting on the PO for every call.

## Learn from incidents, reduce recurrence
Retrospect on production issues to add prevention work (product or process) and improve your service rules and DoD.

## Service level shapes team organization
24/7 high-SLA products require more support capacity and different on-call/response design than low-SLA products.

---
# Scrum events: effective roles and behaviors
## Sprint Planning I (Why/What): PO leads the “why”
- Align on Sprint Goal and selected items (stakeholders may join for clarity).
- Split oversized items; move excess back to Product Backlog.
- Changing the goal is allowed if “how” reveals it’s unrealistic.

## Sprint Planning II (How): Developers lead the plan
- Do lightweight design, identify tasks, and build the Sprint Backlog.
- PO avoids prescribing technical solutions; collaborate on trade-offs only if scope/goal must adapt.

## Daily Scrum: developers self-manage; PO observes lightly
- Developers plan the next 24 hours to meet the Sprint Goal.
- PO can observe for context, but avoid turning it into a status meeting to the PO.
- Follow up after the meeting if PO input is needed.

## Sprint Review: stakeholders co-create direction
- Demo working, end-to-end increments; whenever possible let stakeholders use it hands-on.
- Capture feedback as PBIs; don’t “silently fix” outside the backlog.
- PO commonly facilitates; SM can support.

## Retrospective: one team, shared improvement
- Clarify purpose upfront; focus on team-controllable actions.
- Go for quality, not quantity—one high-impact action beats many vague ones.
- Address root causes (e.g., Five Whys), not just symptoms; track actions in Sprint or Product Backlog.

---
# Quality and direction: Definition of Done and Sprint Goal
## DoD is the guardrail for every increment
Make your acceptance criteria (incl. NFRs, testing standards, documentation, etc.) explicit so the team can self-check “done.”

## Sprint Goal provides intent, not a task list
Frame a clear “why” so the team can self-organize trade-offs, adjust scope, and still achieve the intended outcome.

## Lead with economic clarity
Know your sprint cost and be ready to explain “why this investment now” in one or two sentences; it sharpens Sprint Goal and focus.

## Separate hats if you wear two
If the PO also develops or tests, state which hat you’re wearing in each conversation to avoid role confusion and better decisions.

## It’s okay not to finish everything
Commit to doing your best and to adapting: drop low-priority work back to the Product Backlog or pull in more if you finish early.

---
