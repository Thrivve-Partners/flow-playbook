---
name: flow-checkin-effectiveness
description: Evaluates standup (Flow Check-in) transcript effectiveness against flow standards. Use when user asks to "analyze this standup", "evaluate flow check-in", "score this standup transcript", "review our daily standup", or wants coaching feedback on standup practices. Provides what's working, what could be improved, specific coaching opportunities, and effectiveness score out of 10.
---

# Flow Check-in Effectiveness Analysis

## Purpose

Evaluate standup (Flow Check-in) transcripts against the standards defined in `Flow Checkin.md` and provide actionable coaching feedback with an effectiveness score.

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

The skill evaluates standups against **6 core areas** totalling **10 points:**

### 1. Invisible Work Check (1 point)
Did the team check for work not on the board? Was the 30-minute rule applied?

**Reference:** Flow Checkin.md - "Before We Look at the Board"

### 2. Question 1: What's Stuck or Ageing? (3 points)
**a) Ageing Items Identified (1 point):** Are they walking oldest items first? Referencing age metrics?

**b) Blocker Management (1 point):** Are blockers specifically named, owned, and categorised (Level 1/2/3)?

**c) Swarming on Ageing Work (1 point):** When work isn't moving, does the team offer to swarm?

**Reference:** Flow Checkin.md - "The Three Questions - 1. What's stuck or ageing?"

### 3. Question 2: WIP Limits & Policies (2 points)
**a) WIP Limit Check (1 point):** Did they check if they're within WIP limits?

**b) Pull Policy & Criteria (1 point):** Is "finish before pull" applied? Are pull criteria referenced?

**Reference:** Flow Checkin.md - "The Three Questions - 2. Are we within our WIP limits, and using our Policies effectively?"

### 4. Question 3: What's Moving Today? (1 point)
Is the team clear on what progresses today? Do people leave knowing exactly what they're working on?

**Reference:** Flow Checkin.md - "The Three Questions - 3. What's moving today?"

### 5. Pattern Recognition (1 point)
Are recurring patterns noted for flow review (not solved in standup)?

**Reference:** Flow Checkin.md - "When the Conversation Goes Deeper"

### 6. Overall Health (2 points)
**a) Routine Feel & Honest Board (1 point):** Does it feel routine? Is work moving? Are blockers named early?

**b) Clear Next Steps (1 point):** Does the team leave knowing exactly what the day looks like?

**Reference:** Flow Checkin.md - "What Good Looks Like"

## Detailed Scoring Criteria

For detailed scoring criteria, evidence to capture, and examples for each section, see:
`references/flow-checkin-rubric.md`

## Output Structure

### 1. What's Working
List positive observations with evidence:
- **[Category]:** [Specific behaviour observed]
  - **Evidence:** "[Direct quote from transcript]"
  - **Why this matters:** [Reference to Flow Check-in standard]

**Example:**
- **Swarming Visible:** Louise recognised team helping each other
  - **Evidence:** "I really like the way that we've been working this week and gurgling down. Leila, you've been helping Shweta"
  - **Why this matters:** Flow Check-in standard - "Work as a team on what's already in flight" (Question 2)

### 2. What Could Be Improved
List gaps identified with evidence:
- **[Category]:** [Specific gap observed]
  - **Evidence:** "[Direct quote showing gap or absence]"
  - **Flow Check-in standard:** [Reference to specific section]

**Example:**
- **No Work Item Age Focus:** Standup walked columns, not age
  - **Evidence:** Board walk: "Ready for Release → NF Testing → In Test → In Development" (no mention of age)
  - **Flow Check-in standard:** "Look at the board and identify anything that isn't moving as expected. At 50% of SLE: flag it." (Question 1)

### 3. Coaching Opportunities
Specific, actionable suggestions with references:
- **[What to coach]:** [Specific action]
  - **When:** [Specific trigger in standup]
  - **What to say:** "[Example coaching phrase]"
  - **Reference:** [Flow Check-in section]

**Example:**
- **Introduce Age-Based Walk:** Start standup with Work Item Age chart
  - **When:** At standup start (before column walk)
  - **What to say:** "Let's start with the Work Item Age chart - what's the oldest item on the board?"
  - **Reference:** Question 1 - "Look at the board and identify anything that isn't moving as expected"

### 4. Effectiveness Score

**Score: X/10**

**Breakdown:**
1. Invisible Work Check: X/1
2. Question 1 (Stuck/Ageing): X/3
   - Ageing items identified: X/1
   - Blocker management: X/1
   - Swarming on ageing work: X/1
3. Question 2 (WIP & Policies): X/2
   - WIP limit check: X/1
   - Pull policy & criteria: X/1
4. Question 3 (Moving Today): X/1
5. Pattern Recognition: X/1
6. Overall Health: X/2
   - Routine feel & honest board: X/1
   - Clear next steps: X/1

**Interpretation:**
- **8-10:** Excellent - Flow Check-in standards well embedded, minor refinements only
- **6-7:** Good - Core practices present, needs consistent application
- **4-5:** Developing - Some practices emerging, significant coaching needed
- **2-3:** Early - Few practices present, intensive coaching required
- **0-1:** Not Present - Flow Check-in standards not yet introduced

**Key Priority for Next Session:**
[1-2 most impactful coaching opportunities]

## How to Use This Skill

1. **Read the standup transcript** (provided by user)
2. **Read Flow Checkin.md** to refresh on standards (located in same directory as this skill)
3. **Evaluate transcript** against each criterion using the detailed rubric (see `references/flow-checkin-rubric.md`)
4. **Capture evidence** (direct quotes) for each observation
5. **Generate output** in the structure above
6. **Provide specific, actionable coaching** tied to Flow Check-in sections
7. **Consider context** (team's week in pilot, established practices, recent changes)

## Important Guidelines

- **Be evidence-based:** Always quote directly from transcript
- **Reference standards:** Cite specific Flow Check-in sections
- **Be actionable:** Coaching should be specific enough to apply in next standup
- **Context matters:** Consider team context (week in pilot, established practices)
- **Honest assessment:** Don't inflate scores - gaps are coaching opportunities
- **UK British English:** Use British spelling (organised, recognise, behaviour, prioritise, etc.) and conventions throughout all output

## Example Analyses

See these example analyses for reference on output structure and level of detail:
- `03-Pilot-Execution/Coaching-Sessions/Platform 2/Platform-2-Flow-Checkin-Analysis-20260227.md` (Score: 2.5/10 - Early)
- `03-Pilot-Execution/Coaching-Sessions/C2C/C2C-Flow-Checkin-Analysis-20260302.md` (Score: 5.5/10 - Developing)

These demonstrate:
- How to structure evidence-based observations
- Appropriate level of detail in coaching opportunities
- How to use British English throughout
- Progression from Early (2.5) to Developing (5.5) over 3 weeks of coaching

## Troubleshooting

**Issue:** Transcript is too short or informal
**Solution:** Note that brief standups may not surface all practices. Focus on what's present and coach on foundational practices first.

**Issue:** Can't determine if something was done (not mentioned in transcript)
**Solution:** Score as not present (0 points). If it's not captured in the transcript, it either didn't happen or wasn't explicit enough to be observable.

**Issue:** Team is very early in flow adoption
**Solution:** Expect low scores (2-3/10). Focus coaching on 1-2 foundational practices (invisible work check, age-based walk) rather than overwhelming with all practices.

**Issue:** Multiple things need improvement
**Solution:** Prioritise 1-2 highest-impact coaching opportunities in "Key Priority for Next Session". Don't overwhelm the team.

## References

- **Flow Checkin.md** - The standards document defining all evaluation criteria
- **references/flow-checkin-rubric.md** - Detailed scoring criteria and examples for each evaluation area
