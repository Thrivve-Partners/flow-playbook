---
name: flow-checkin-effectiveness
description: Evaluates standup (Flow Check-in) transcript effectiveness against flow standards. Use when user asks to "analyze this standup", "evaluate flow check-in", "score this standup transcript", "review our daily standup", or wants coaching feedback on standup practices. Provides what's working, what could be improved, specific coaching opportunities, and effectiveness score out of 10.
---

# Flow Check-in Effectiveness Analysis

## Purpose

Evaluate standup (Flow Check-in) transcripts against the standards defined in the Flow Check-In guide (v1.4) and provide actionable coaching feedback with an effectiveness score.

This skill helps identify:
- Which flow practices are working well (with evidence)
- Where gaps exist compared to flow standards
- Specific, actionable coaching opportunities tied to standards
- Overall effectiveness score (0-10 scale)

## When to Use This Skill

Use this skill when you have:
- A standup transcript to analyze
- Questions about standup effectiveness
- Need for coaching feedback on flow practices
- Want to track standup improvement over time

**Trigger phrases:**
- "Analyze this standup transcript"
- "Evaluate flow check-in effectiveness"
- "Score this standup"
- "Review our daily standup"
- "How effective was this standup?"

## Input Required

**Essential:**
1. **Standup transcript file path** - The transcription to analyze

**Optional (provides context):**
2. **Team context:**
   - Team name
   - SLE (85th percentile cycle time)
   - WIP limits (if established)
   - Week number in pilot or flow practice adoption

## Evaluation Framework

The skill evaluates standups against **10 criteria** totalling **10 points**, aligned to the Flow Check-In v1.4 running order:

### 1. Step 0 — Invisible Work Check (1 point)
Did the team check for work not on the board before the board walk? Was the 30-minute rule applied?

### 2. Step 1 — Finishing Focus / Right-to-Left Walk (1 point)
Did the facilitator open the board walk with the last column (ready-for-release or equivalent) and work right-to-left? Was the framing about finishing and helping to land, not about ageing risk? A walk that opens with pace-percentile-ordered ageing items, or column-by-column from the left, does not meet the v1.4 Step 1 standard.

### 3. Step 2a — Ageing Items: Three Lenses (1 point)
Are they using the three lenses from the v1.4 standard?
- **Lens 1 — Overall Age (SLE):** Items flagged at 50% and 70% of SLE?
- **Lens 2 — Stage Pace:** Pace percentiles referenced? Items beyond 70th pace percentile flagged?
- **Lens 3 — Staleness:** Staleness threshold applied? Stale items surfaced?

Two or more lenses used systematically = full mark. One lens = partial.

### 4. Step 2b — Blocker Management (1 point)
Are blockers named, owned, and categorised (Level 1/2/3)? Is the blocked-vs-ageing distinction applied?

### 5. Step 2c — Swarming on Ageing Work (1 point)
When work isn't moving, does the team swarm? At 70% SLE, does everything else wait?

### 6. Step 3a — WIP Limit Check (1 point)
Stage-level WIP scan? Over/under addressed?

### 7. Step 3b — Pull Criteria & Policies (1 point)
Finish-before-pull applied? Pull criteria referenced? Ticket movement discipline?

### 8. Step 3c — Replenishment (1 point)
Explicit replenishment question asked ("Does anyone need work?")? Next item identified by priority/business value? Backlog readiness discussed if needed?

### 9. Step 4 — What's Moving Today (1 point)
Structured close with per-person commitments? Everyone leaves knowing what they're working on?

### 10. Session Texture — Integrated Walk + After-Party + Routine Feel (1 point)
Is this one integrated conversation walking the board, or two events shoved together (a chart narration followed by a per-person status round)? When depth is needed, is the after-party used? Does the session feel routine and team-owned, or DM-narrated with the team listening?

## Detailed Scoring Criteria

For detailed scoring criteria, evidence to capture, and examples for each criterion, see:
`references/flow-checkin-rubric.md`

## Output Structure

### 1. What's Working
List positive observations with evidence:
- **[Category]:** [Specific behaviour observed]
  - **Evidence:** "[Direct quote from transcript]"
  - **Why this matters:** [Reference to Flow Check-in standard]

**Example:**
- **Finishing Focus:** Facilitator opened the walk with the last column
  - **Evidence:** *"What's in ready-for-release? Can anything cross the line today?"*
  - **Why this matters:** Flow Check-in v1.4 Step 1 — *"Walk the board from right to left. Start with the last column before done."*

### 2. What Could Be Improved
List gaps identified with evidence:
- **[Category]:** [Specific gap observed]
  - **Evidence:** "[Direct quote showing gap or absence]"
  - **Flow Check-in standard:** [Reference to specific section]

**Example:**
- **Ageing-First Walk (v1.4 anti-pattern):** Standup walked pace-percentile descending, not right-to-left
  - **Evidence:** *"Let's go based on the pace percentile. The highest one on this list at the minute is..."*
  - **Flow Check-in v1.4:** Step 1 — *"Walk the board from right to left. Start with the last column before done."*

### 3. Coaching Opportunities
Specific, actionable suggestions with references:
- **[What to coach]:** [Specific action]
  - **When:** [Specific trigger in standup]
  - **What to say:** "[Example coaching phrase]"
  - **Reference:** [Flow Check-in section]

**Example:**
- **Flip the Walk Order:** Start with ready-for-release, walk back through the board
  - **When:** At the opening of Step 1, every session
  - **What to say:** *"What's in ready-for-release? Can anything cross the line today? Then one step back — what's in test or review?"*
  - **Reference:** Flow Check-in v1.4 Step 1 — *"Walk the board from right to left. Start with the last column before done."*

### 4. Effectiveness Score

**Score: X/10**

**Breakdown:**

| # | Area | Score | Notes |
|---|------|-------|-------|
| 1 | Invisible Work Check | X/1 | |
| 2 | Finishing Focus / Right-to-Left Walk | X/1 | |
| 3 | Ageing Items — Three Lenses | X/1 | |
| 4 | Blocker Management | X/1 | |
| 5 | Swarming on Ageing Work | X/1 | |
| 6 | WIP Limit Check | X/1 | |
| 7 | Pull Criteria & Policies | X/1 | |
| 8 | Replenishment | X/1 | |
| 9 | What's Moving Today | X/1 | |
| 10 | Session Texture | X/1 | |
| | **Total** | **X/10** | |

**Interpretation:**
- **8–10:** Excellent — Flow Check-in standards well embedded, minor refinements only
- **6–7:** Good — Core practices present, needs consistent application
- **4–5:** Developing — Some practices emerging, significant coaching needed
- **2–3:** Early — Few practices present, intensive coaching required
- **0–1:** Not Present — Flow Check-in standards not yet introduced

**Key Priority for Next Session:**
[1–2 most impactful coaching opportunities]

## How to Use This Skill

1. **Read the standup transcript** (provided by user)
2. **Read the Flow Check-In v1.4 guide** to refresh on standards (located at `01-Client-Intelligence/Reference/Standards/Flow Checkin v1.4.md`)
3. **Evaluate transcript** against each criterion using the detailed rubric (see `references/flow-checkin-rubric.md`)
4. **Capture evidence** (direct quotes) for each observation
5. **Generate output** in the structure above
6. **Provide specific, actionable coaching** tied to Flow Check-in sections
7. **Consider context** (team's week in pilot, established practices, recent changes)

## Important Guidelines

- **Be evidence-based:** Always quote directly from transcript
- **Reference standards:** Cite specific Flow Check-in v1.4 sections (Step 0, Step 1, etc.)
- **Be actionable:** Coaching should be specific enough to apply in next standup
- **Context matters:** Consider team context (week in pilot, established practices)
- **Honest assessment:** Don't inflate scores — gaps are coaching opportunities
- **UK British English:** Use British spelling (organised, recognise, behaviour, prioritise, etc.) and conventions throughout all output
- **Rubric versioning:** Analyses before 22 April 2026 used the v1.3 rubric. The 10-point scale is preserved in v1.4, but two structural changes affect cross-version comparability:
  1. **Finishing Focus (Step 1 right-to-left walk)** is now scored explicitly as criterion 2. Sessions that walked ageing-first (e.g. pace-percentile descending, or column-by-column from the left) will score lower under v1.4 than they would have under v1.3. This is intentional — the v1.4 standard defines right-to-left as the correct walk order, and the anti-pattern needs to show up in the score.
  2. **Pattern Recognition & After-Party** and **Overall Health** have been merged into a single **Session Texture** criterion (criterion 10) that explicitly tests the two-events-shoved-together anti-pattern (chart narration followed by per-person status round).

  Score-trajectory tables should note the rubric version change explicitly. A v1.3 score of 7.5 and a v1.4 score of 7.5 may describe sessions with different shapes — the v1.4 version prioritises finishing focus and integrated walk in ways the v1.3 rubric did not.

## Example Analyses

See these example analyses for reference on output structure and level of detail:
- `03-Pilot-Execution/Coaching-Sessions/Platform 2/standups/Platform-2-Flow-Checkin-Analysis-20260227.md` (Score: 2.5/10 — Early, pre-v1.3 rubric)
- `03-Pilot-Execution/Coaching-Sessions/C2C/standups/C2C-Flow-Checkin-Analysis-20260302.md` (Score: 5.5/10 — Developing, pre-v1.3 rubric)
- `03-Pilot-Execution/Coaching-Sessions/Micro-Shippers/standups/Micro-Shippers-Flow-Checkin-Analysis-20260330.md` (Score: 6.5/10 — Good, pre-v1.3 rubric)

These demonstrate:
- How to structure evidence-based observations
- Appropriate level of detail in coaching opportunities
- How to use British English throughout
- Progression across teams and facilitators

## Troubleshooting

**Issue:** Transcript is too short or informal
**Solution:** Note that brief standups may not surface all practices. Focus on what's present and coach on foundational practices first.

**Issue:** Can't determine if something was done (not mentioned in transcript)
**Solution:** Score as not present (0 points). If it's not captured in the transcript, it either didn't happen or wasn't explicit enough to be observable.

**Issue:** Team is very early in flow adoption
**Solution:** Expect low scores (2–3/10). Focus coaching on 1–2 foundational practices (invisible work check, right-to-left walk) rather than overwhelming with all practices.

**Issue:** Multiple things need improvement
**Solution:** Prioritise 1–2 highest-impact coaching opportunities in "Key Priority for Next Session". Don't overwhelm the team.

**Issue:** Facilitator walks ageing-first (pace-percentile descending or oldest-first)
**Solution:** This is the v1.4 anti-pattern explicitly called out. Score criterion 2 (Finishing Focus) accordingly — typically 0.0 unless the last column was still surfaced early in the walk. Even strong facilitators frequently default to ageing-first; flag it in coaching and reference the v1.4 Step 1 wording.

**Issue:** Session runs as a chart narration followed by a per-person status round
**Solution:** This is the v1.4 two-events-shoved-together anti-pattern. Score criterion 10 (Session Texture) accordingly — typically 0.0 to 0.5. The structural elements may all be present but the practice has fragmented. Coach on integrating: each person contributes as their item is walked.

**Issue:** Comparing scores across rubric versions
**Solution:** The 10-point scale is preserved, but v1.4 scoring is stricter on finishing focus and session texture. When presenting score trajectories across the rubric change, note the version transition date (22 April 2026) and don't treat pre-v1.4 scores as directly comparable for those two criteria.

## References

- **Flow Check-In v1.4** — The standards document defining all evaluation criteria (`01-Client-Intelligence/Reference/Standards/Flow Checkin v1.4.md`)
- **references/flow-checkin-rubric.md** — Detailed scoring criteria and examples for each evaluation area
