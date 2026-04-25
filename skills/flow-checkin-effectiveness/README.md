# Flow Check-in Effectiveness Skill

A Claude Code skill for evaluating standup (Flow Check-in) transcripts against flow standards and providing actionable coaching feedback.

## What This Skill Does

Evaluates standup transcripts and provides:
- **What's Working:** Evidence-based observations of effective practices
- **What Could Be Improved:** Gaps identified with specific evidence
- **Coaching Opportunities:** Actionable suggestions tied to flow standards
- **Effectiveness Score:** 0-10 rating with detailed breakdown

## Installation

### Option 1: Install via Claude Code CLI (Recommended)

```bash
claude-code skills install /path/to/flow-checkin-effectiveness
```

### Option 2: Manual Installation

1. Copy the `flow-checkin-effectiveness/` folder to your Claude Code skills directory:
   - **macOS/Linux:** `~/.claude/skills/`
   - **Windows:** `%USERPROFILE%\.claude\skills\`

2. Restart Claude Code or reload skills

## Usage

### Basic Usage

```
Analyze this standup transcript: [path to transcript]
```

### With Context

```
Evaluate this flow check-in for Platform 2 team (Week 5, SLE 59 days):
[transcript path or paste transcript]
```

### Other Trigger Phrases

- "Score this standup"
- "Review our daily standup"
- "How effective was this standup?"
- "Evaluate flow check-in effectiveness"

## Example Output

```
## 1. What's Working

### Swarming Explicitly Requested (Question 1c)
**Evidence:** "Can we swarm on this to do please?"
**Why this matters:** Flow Check-in standard - "Work as a team on what's already in flight"

## 2. What Could Be Improved

### No Invisible Work Check
**Evidence:** No one asked "Is there anything you're working on that isn't on the board?"
**Flow Check-in standard:** "Before We Look at the Board - Is there anything you're working on that isn't on it?"

## 3. Coaching Opportunities

### Introduce Invisible Work Check at Standup Start
- **When:** Before looking at the board
- **What to say:** "Before we look at the board - is anyone working on anything that isn't on it?"
- **Reference:** Flow Check-in "Before We Look at the Board"

## 4. Effectiveness Score

**Score: 5.5/10** - **Developing**

**Breakdown:**
1. Invisible Work Check: 0/1
2. Question 1 (Stuck/Ageing): 2.0/3
3. Question 2 (WIP & Policies): 0.5/2
4. Question 3 (Moving Today): 1.0/1
5. Pattern Recognition: 1.0/1
6. Overall Health: 1.0/2

**Key Priority for Next Session:**
1. Introduce invisible work check (30 seconds, foundational)
2. Make WIP limits visible and check them
```

## Scoring Framework

The skill evaluates 6 core areas (10 points total):

1. **Invisible Work Check** (1 point) - Work not on the board?
2. **Question 1: What's Stuck or Ageing?** (3 points)
   - Ageing items identified (1 point)
   - Blocker management (1 point)
   - Swarming on ageing work (1 point)
3. **Question 2: WIP Limits & Policies** (2 points)
   - WIP limit check (1 point)
   - Pull policy & criteria (1 point)
4. **Question 3: What's Moving Today?** (1 point)
5. **Pattern Recognition** (1 point)
6. **Overall Health** (2 points)
   - Routine feel & honest board (1 point)
   - Clear next steps (1 point)

### Interpretation

- **8-10:** Excellent - Standards well embedded
- **6-7:** Good - Core practices present, needs consistency
- **4-5:** Developing - Some practices emerging, significant coaching needed
- **2-3:** Early - Few practices present, intensive coaching required
- **0-1:** Not Present - Standards not yet introduced

## Requirements

This skill requires:
- **Flow Checkin.md** - The standards document (referenced for evaluation criteria)
- **Standup transcript** - Meeting transcription or notes to analyze

The skill uses UK British English for all outputs.

## Example Analyses

See these examples in the Evri project:
- `Platform-2-Flow-Checkin-Analysis-20260227.md` (Score: 2.5/10 - Early)
- `C2C-Flow-Checkin-Analysis-20260302.md` (Score: 5.5/10 - Developing)

## Files

- **SKILL.md** - Main skill instructions with YAML frontmatter
- **references/flow-checkin-rubric.md** - Detailed scoring criteria and examples
- **README.md** - This file (installation and usage guide)

## Support

For questions or issues:
- Check the detailed rubric: `references/flow-checkin-rubric.md`
- Review example analyses in `03-Pilot-Execution/Coaching-Sessions/`
- Reference flow standards: `Flow Checkin.md`

## Version

v1.0.0 - Initial release (March 2026)
v1.1.0 - Changes based on v1.4 of the Flow Checkin
