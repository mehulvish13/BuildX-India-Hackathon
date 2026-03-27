## Plan: AlphaSense AI Winning Build

Build AlphaSense AI as a multi-agent investor copilot for Problem 6 that delivers WHY + RISK + ACTION, demonstrates self-correction, and proves measurable portfolio impact with explicit assumptions.

**Steps**
1. Phase 0 - Positioning lock (2 hours): Freeze product claim as "signal-finder and action assistant, not market summarizer".
2. Phase 0 - MVP boundary lock (depends on 1): Keep one complete pipeline only: detect signal -> validate pattern -> reason -> risk check -> portfolio-aware action -> audit log.
3. Phase 1 - Agent contract design (Day 1): Define five core agents and one memory loop.
4. Phase 1 - Agent roles:
- Signal Agent: ingest filings, insider activity, and earnings events.
- Pattern Agent: detect breakout/reversal/support-resistance style technical setups.
- Reasoning Agent: generate evidence-based WHY narrative with source pointers.
- Risk Agent: assign downside level (low/medium/high), identify key failure conditions.
- Portfolio Agent: map recommendation to user profile (watch, buy small, avoid).
- Memory Loop: store outcome feedback and tune scoring thresholds for future runs.
5. Phase 1 - Data schemas (depends on 3): Finalize OpportunityCard fields: symbol, confidence, WHY points, RISK points, ACTION, position sizing hint, timestamp, evidence references.
6. Phase 2 - Vertical slice implementation (Days 2-3, depends on 5): Build deterministic replay for 3 scenarios where agents produce complete OpportunityCard output.
7. Phase 2 - Self-correction demo path (depends on 6): Force one critic-style failure by injecting weak evidence; rerun loop so Reasoning or Risk output is corrected before final recommendation.
8. Phase 3 - Human-in-the-loop gate (Day 4): Add explicit approval checkpoint before any action changes portfolio suggestion state from draft to approved.
9. Phase 3 - Impact model build (parallel with 8): Add KPI calculations and baseline comparison from replay runs.
10. Phase 4 - Pitch packaging (Day 5): Assemble 3-minute script and architecture document centered on autonomy, recovery, and business value.
11. Phase 4 - Final hardening (Day 6): Rehearse full demo three times with stable dataset and lock final submission assets.

**Winning demo flow (3 minutes)**
1. Problem pain: investor overload and missed opportunities.
2. Live run: Opportunity detected for one stock with WHY evidence chain.
3. Risk reveal: downside conditions and risk level.
4. Personalized action: watch or buy small or avoid based on portfolio profile.
5. Failure-recovery: show weak recommendation rejected and corrected.
6. Impact math: show annual loss-avoidance or opportunity-capture uplift.

**Impact model**
1. Missed-opportunity avoidance: monthly missed opportunities x average expected return x portfolio size x 12.
2. Analyst time saved: manual signal triage minutes minus agent triage minutes, multiplied by opportunities per month.
3. Decision quality uplift: accepted recommendations after correction minus accepted recommendations before correction.
4. Risk containment: high-risk recommendations downgraded or blocked by Risk Agent as percent of total risky candidates.

**Must-have scope**
- Full five-agent orchestration.
- WHY + RISK + ACTION output format.
- One self-correction cycle visible in demo.
- Human approval gate.
- Full audit log by agent and timestamp.
- Quantified impact model with assumptions.

**Nice-to-have scope**
- Voice input.
- Auto short-video market summary.
- Regional language output.

**Relevant files**
- README.md — update to include architecture, run steps, replay scenarios, impact formulas, and 3-minute demo flow.

**Verification**
1. Run three replay scenarios and confirm all five agents emit outputs.
2. Trigger one low-confidence reasoning output and verify corrected final output.
3. Validate approval gate blocks unapproved action recommendations.
4. Recompute impact numbers from logs and cross-check assumptions.
5. Ensure video, architecture document, and repository narrative align exactly with judged criteria.

**Decisions**
- Track: Problem 6 (AI for the Indian Investor).
- Product: AlphaSense AI - Investor Copilot.
- Core differentiator: WHY + RISK + ACTION with self-improving agent loop.
- Scope focus: intelligence depth and measurable impact over UI breadth.

**Further Considerations**
1. Keep recommendations advisory only, not auto-trading, to reduce policy risk.
2. Use an offline replay dataset for deterministic final demo reliability.
3. If schedule slips, merge Pattern and Reasoning into one agent but preserve Risk and Memory loop.