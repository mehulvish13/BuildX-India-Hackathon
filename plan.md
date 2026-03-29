## Plan: Autonomous Meeting Workflow MVP

Build a Problem 2 submission where multi-agents convert meeting inputs into tracked execution with autonomous follow-up, stall detection, and escalation, while maintaining a full audit trail. Use Python backend with a minimal web UI and deterministic replay mode (no external APIs) to maximize demo reliability.

**Steps**
1. Phase 0 - Product lock (2 hours): Freeze thesis: "From raw meeting notes to completed tasks with autonomous follow-up and SLA escalation."
2. Phase 0 - Scope lock (depends on 1): Limit to one workflow only: ingest meeting transcript -> extract decisions/tasks -> assign owners -> follow-up loop -> escalate stalled tasks -> status dashboard.
3. Phase 1 - Agent design (Day 1): Define 5 agents.
4. Phase 1 - Agent roles:
- Intake Agent: parses transcript/notes into normalized meeting artifacts.
- Decision Agent: extracts decisions, tasks, owners, due dates, dependencies.
- Orchestrator Agent: creates execution plan and schedules follow-up checks.
- Recovery Agent: detects stalls/failures and performs retry/reroute/escalation.
- Audit Agent: logs every decision, confidence, and action with timestamps.
5. Phase 1 - Data contracts (depends on 3): Finalize schemas for MeetingInput, TaskItem, WorkflowState, Alert, EscalationEvent, AuditEntry.
6. Phase 2 - Vertical slice build (Days 2-3, depends on 5): Implement deterministic replay scenarios for 3 cases:
- Happy path completion
- Owner misses deadline, recovered via reminder
- Repeated delay, escalated to manager
7. Phase 2 - Autonomy depth (depends on 6): Ensure at least 4 consecutive steps execute without manual intervention.
8. Phase 3 - Failure recovery hardening (Day 4): Add policy for retry windows, escalation thresholds, and fallback owner routing.
9. Phase 3 - Human control gate (parallel with 8): Add explicit approval for high-impact actions (final escalation or reassignment).
10. Phase 4 - Impact model (Day 5): Quantify:
- Follow-up automation rate
- Delay reduction percentage
- Coordination time saved per week
11. Phase 4 - Packaging and rehearsal (Day 6): Finalize README narrative, architecture document, and 3-minute demo runbook aligned to judges.

**Winning differentiators**
1. Explicit self-correction loop: missed SLA triggers automatic retry and escalation path.
2. Full auditability: every agent action is explainable and timestamped.
3. Real autonomy: workflow continues without human prompts until a policy gate is hit.

**Must-have vs Nice-to-have**
- Must-have: multi-agent orchestration, stall detection, autonomous recovery, approval gate, audit trail, impact math.
- Nice-to-have: calendar/email integration adapters, LLM-based owner disambiguation, analytics UI polish.

**Relevant files**
- README.md — should be rewritten to reflect Problem 2 solution narrative and demo flow.
- plan.md — optional user-facing project plan mirror if you want repo-visible planning.

**Verification**
1. Run 3 replay scenarios and confirm end-to-end completion with correct state transitions.
2. Force a task delay and verify Recovery Agent retries then escalates per policy.
3. Confirm audit log captures agent, rationale, confidence, and outcome for all major transitions.
4. Validate KPI calculations from scenario outputs and ensure assumptions are explicit.
5. Rehearse 3-minute demo twice under time with one failure-recovery sequence included.

**Decisions**
- Selected problem: Problem 2 (Agentic AI for Autonomous Enterprise Workflows).
- Chosen workflow: Meeting-to-Execution.
- Build constraints: No external APIs; deterministic replay mode.
- Stack: Python backend + minimal web UI.

**Further Considerations**
1. Keep deterministic replay as primary demo path; external integrations can be shown as adapters only.
2. Use synthetic but realistic meeting data with varied ownership and SLA windows.
3. If timeline slips, merge Intake + Decision into one agent, but keep Recovery + Audit separate for judging impact.