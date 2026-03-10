# founder-discovery

Talk to users before you build. Customer discovery skill for Claude Code — Mom Test interviews, survey design, Jobs-to-be-Done mapping, and research synthesis.

## Commands

| Command | What it does |
|---------|-------------|
| `/discovery:interview` | Mom Test interview scripts + question banks |
| `/discovery:survey` | Survey design with bias prevention |
| `/discovery:jobs` | Jobs-to-be-Done mapping + switch analysis |
| `/discovery:analyze` | Synthesize research into actionable insights |
| `/discovery:help` | Command reference |

## Install

```bash
npx skills add ORBWEVA/founder-discovery
```

Or manually copy:
- `skills/` -> `~/.claude/skills/`
- `commands/` -> `~/.claude/commands/`

## Example output

### `/discovery:jobs` for a project management SaaS

```
JOBS-TO-BE-DONE MAP
=====================
CORE JOB STATEMENT:
  "When I'm juggling 5+ client projects with a team of 3,
  I want to see who's overloaded before they burn out,
  so I can reassign work without missing deadlines."

FUNCTIONAL JOB: Track team capacity across projects in real time
EMOTIONAL JOB:  Feel in control without micromanaging
SOCIAL JOB:     Be seen as a manager who doesn't let things slip

JOB MAP
========
Step              | What they do              | Pain | Current solution
──────────────────┼───────────────────────────┼──────┼─────────────────
1. Define         | Scope new project         | 2/5  | Google Doc template
2. Locate         | Find who's available      | 5/5  | Slack each person
3. Prepare        | Assign tasks              | 3/5  | Spreadsheet
4. Confirm        | Check assignments stick   | 4/5  | Monday standup
5. Execute        | Team does the work        | 2/5  | Existing tools
6. Monitor        | Track progress            | 5/5  | Manual check-ins
7. Modify         | Reassign when behind      | 4/5  | Fire drill meetings
8. Conclude       | Close out and retro       | 1/5  | Skipped usually

HIGHEST PAIN STEP: 2 (Locate) + 6 (Monitor) — both 5/5
Product should focus on real-time capacity visibility.

FORCES OF PROGRESS
====================
Push of situation:    "I found out someone was at 150% only    Strength: 5/5
                       after they missed a deadline"
Pull of new solution: "One dashboard showing who has bandwidth" Strength: 4/5
Allegiance to current:"We've customized our spreadsheet a lot"  Strength: 3/5
Anxiety of change:    "Migration + getting team to adopt"       Strength: 2/5

TOTAL PUSH: 9/10    TOTAL RESIST: 5/10
Customers will switch with the right trigger event.
```

### `/discovery:interview` for a fitness app

```
INTERVIEW SCRIPT
=================
Duration: 30 minutes
Target: People who started and quit a workout program in the last 6 months

WARM-UP (2 min)
  "Thanks for chatting. I'm trying to understand how people
  manage their fitness routines. No sales pitch — I just
  want to learn from your experience."

PROBLEM EXPLORATION (15 min)
  "Tell me about the last workout program you tried."
  "What made you start it?"
  "Walk me through a typical week — what actually happened?"
  "When did you first feel like it wasn't working?"
  "What did you try to get back on track?"
  "What are you doing now instead?"

COMMITMENT EXTRACTION (3 min)
  "If something solved [specific pain they mentioned],
  what would you expect to pay for it?"
  "Who else do you know who's dealt with this?"

POST-INTERVIEW NOTES
  Commitment level: [referral / beta signup / payment intent / nothing]
  Key insight: ___
  Emotion detected: ___
  Quote to remember: "___"
```

## How the commands connect

```
DISCOVER:  /discovery:interview → /discovery:survey (quantify patterns)
MAP:       /discovery:jobs (map what users are hiring you for)
DECIDE:    /discovery:analyze (turn data into product decisions)
```

1. **Discover** — interview 10-20 users, then survey to quantify what you heard
2. **Map** — structure findings into Jobs-to-be-Done with pain scores
3. **Decide** — synthesize everything into personas, priorities, and next steps

## Pairs with other ORBWEVA skills

| Skill | How it connects |
|-------|----------------|
| [dt-skill](https://github.com/ORBWEVA/dt-skill) | Discovery personas feed into `/dt:empathize` and `/dt:define` |
| [gtm-skills](https://github.com/ORBWEVA/gtm-skills) | `/discovery:analyze` personas feed into `/gtm:positioning` ICP |
| [founder-metrics](https://github.com/ORBWEVA/founder-metrics) | JTBD outcome scores feed into `/startup:pmf` measurement |

## Security

Zero executable code. Pure markdown — structured prompts that guide Claude's thinking. No scripts, no dependencies, no API calls, no shell commands.

```
skills/discovery/SKILL.md          # Discovery methodology (4 stages)
commands/discovery/interview.md    # Mom Test interview scripts
commands/discovery/survey.md       # Survey design + bias prevention
commands/discovery/jobs.md         # Jobs-to-be-Done mapping
commands/discovery/analyze.md      # Research synthesis
commands/discovery/help.md         # Command reference
package.json                       # metadata only
```

## Full founder stack

```bash
npx skills add ORBWEVA/dt-skill              # Design Thinking
npx skills add ORBWEVA/founder-discovery     # Customer Discovery (this skill)
npx skills add ORBWEVA/gtm-skills            # GTM, GEO & SEO
npx skills add ORBWEVA/founder-metrics       # Startup Metrics & Benchmarks
```

## License

MIT
