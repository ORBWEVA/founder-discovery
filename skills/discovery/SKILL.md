---
name: discovery
description: Customer discovery skill for founders. Use when user wants to design user interviews, build surveys, run Jobs-to-be-Done analysis, or synthesize customer research. Triggers on "customer discovery", "user interviews", "Mom Test", "JTBD", "jobs to be done", "customer research", "user research", "survey design", or /discovery commands.
---

# Customer Discovery Skill

Talk to users before you build. Structured frameworks for interviews, surveys, Jobs-to-be-Done, and synthesis — so you build what people actually want.

## Commands

| Command | What it does |
|---------|-------------|
| `/discovery:interview` | Interview script design (Mom Test methodology) |
| `/discovery:survey` | Survey design with bias prevention |
| `/discovery:jobs` | Jobs-to-be-Done mapping and analysis |
| `/discovery:analyze` | Synthesize research into actionable insights |
| `/discovery:help` | Command reference |

---

## Stage 1: User Interviews (`/discovery:interview`)

**Goal:** Design interviews that reveal truth about user behavior — not what they think you want to hear.

### The Mom Test (Rob Fitzpatrick)

Three rules for interviews that don't lie to you:

```
THE MOM TEST RULES
====================
1. Talk about THEIR life, not YOUR idea
   BAD:  "Would you use a tool that does X?"
   GOOD: "How do you currently handle X?"

2. Ask about specifics in the PAST, not hypotheticals
   BAD:  "Would you pay $50/month for this?"
   GOOD: "What did you pay last time you tried to solve this?"

3. Talk less, listen more
   BAD:  Pitching your solution for 20 minutes
   GOOD: Asking one question, then shutting up for 2 minutes
```

### Interview Script Template

```
INTERVIEW SCRIPT
=================
Duration: 30 minutes
Interviewee: [Name, role, company]
Context: [How you found them, what you know about them]

WARM-UP (2 min)
  "Thanks for taking the time. I'm trying to understand how
  [people in your role] handle [problem area]. No pitching —
  I just want to learn from your experience."

CONTEXT (5 min)
  "Tell me about your role. What does a typical [week/day] look like?"
  "What are the biggest challenges you're dealing with right now?"

PROBLEM EXPLORATION (15 min)
  "When was the last time [problem] came up?"
  "Walk me through exactly what happened."
  "What did you try? What worked? What didn't?"
  "How much time/money did that cost you?"
  "What are you using today to handle this?"
  "What's the most annoying part of your current approach?"

SOLUTION VALIDATION (5 min — only if you have something to show)
  "I'm working on something in this space. Can I get your reaction?"
  [Show prototype/mockup — then STOP TALKING and observe]
  "What's your first impression?"
  "What would you use this for?"
  "What's missing?"

COMMITMENT (3 min)
  "Who else should I talk to about this?"
  "Would you be open to trying an early version when it's ready?"
  "Can I follow up with you in [X weeks]?"

POST-INTERVIEW (internal, don't say out loud)
  Commitment level: [referral / beta signup / payment intent / nothing]
  Key insight: ___
  Emotion detected: ___
  Quote to remember: "___"
```

### Question Bank (by stage)

```
PROBLEM DISCOVERY QUESTIONS
==============================
"What's the hardest part about [doing X]?"
"Why is that hard?"
"How often does this come up?"
"What have you tried to solve this?"
"What happened when you tried [solution]?"
"How much time do you spend on this per [week/month]?"
"What does this cost your team/company?"
"If you could wave a magic wand, what would change?"

EXISTING SOLUTION QUESTIONS
==============================
"What tools/processes do you use for this today?"
"How did you end up choosing that?"
"What do you like about it? What do you hate?"
"What do you wish it did differently?"
"How much do you pay for it?"
"Have you considered switching? What stopped you?"

PURCHASE BEHAVIOR QUESTIONS
==============================
"Who decides on tools like this at your company?"
"What's the typical buying process?"
"What would make you switch from what you use today?"
"What would you need to see before paying for this?"
"Have you ever tried to get budget for something like this?"

COMMITMENT EXTRACTION
======================
Weakest → Strongest:
  "That sounds interesting" → WORTHLESS (compliments are noise)
  "Send me info" → WEAK (polite brush-off)
  "I'd try a free version" → MODERATE (low commitment)
  "I'd pay for early access" → STRONG (real commitment)
  "Can I wire you money today?" → JACKPOT (rare but real)
  "Let me introduce you to [decision maker]" → STRONG (action, not words)
```

### Interview Anti-Patterns

```
MISTAKES THAT RUIN INTERVIEWS
================================
[ ] Pitching instead of asking
[ ] Leading questions ("Don't you think X would be better?")
[ ] Accepting compliments as validation ("That's a great idea!")
[ ] Asking hypothetical questions ("Would you use...?")
[ ] Talking to friends/family (they'll be nice, not honest)
[ ] Not recording / taking notes (you'll forget the nuance)
[ ] Interviewing 2-3 people and calling it "research"
[ ] Only talking to people who look like your ICP (survivorship bias)
```

### Sample Size Guide

```
INTERVIEW SAMPLE SIZE
======================
Purpose               | Minimum | Ideal
───────────────────────┼─────────┼──────
Problem validation     | 10      | 20
Solution validation    | 5       | 15
Pricing research       | 10      | 25
Persona identification | 15      | 30

SIGNAL: Stop when you start hearing the same answers.
If interview 8 says what interview 3 said, you have a pattern.
```

### Output
Deliver: Custom interview script + question bank tailored to their product/market + anti-pattern warnings + post-interview synthesis template.

---

## Stage 2: Survey Design (`/discovery:survey`)

**Goal:** Design surveys that produce statistically useful data — not confirmation bias.

### Survey Structure

```
SURVEY DESIGN TEMPLATE
========================
Title: [Clear, non-leading title]
Target: [Who should take this? Be specific.]
Length: [Max 5 minutes / 10-15 questions]
Distribution: [How you'll reach respondents]
Sample target: [Minimum responses needed]

SECTION 1: SCREENING (1-3 questions)
  Filter out people who aren't your ICP.
  "What is your role?" [multiple choice]
  "How many people are on your team?" [range]

SECTION 2: BEHAVIOR (3-5 questions)
  What they ACTUALLY DO (not what they think/feel).
  "How often do you [target behavior]?" [frequency scale]
  "What tools do you currently use for [X]?" [multi-select + other]
  "How much time do you spend on [X] per week?" [range]

SECTION 3: PAIN POINTS (2-3 questions)
  "What's the most frustrating part of [X]?" [open text]
  "Rank these challenges by severity:" [ranking]

SECTION 4: WILLINGNESS (1-2 questions)
  "How would you feel if you could no longer use [current solution]?"
    [Very disappointed / Somewhat / Not disappointed]
  "What would you pay for a tool that [core value prop]?"
    [Price ranges]

SECTION 5: DEMOGRAPHICS (1-2 questions, optional)
  Company size, industry, geography — only if you need it for segmentation.
```

### Bias Prevention

```
SURVEY BIAS CHECKLIST
======================
[ ] No leading questions
    BAD:  "How much do you love our product?"
    GOOD: "How satisfied are you with the product?" [scale]

[ ] No double-barreled questions
    BAD:  "Is the product fast and easy to use?"
    GOOD: Two separate questions for speed and ease

[ ] Balanced answer options
    BAD:  "Great / Good / OK" (no negative option)
    GOOD: "Very satisfied / Satisfied / Neutral / Dissatisfied / Very dissatisfied"

[ ] Randomized option order (where possible)
[ ] "Other" option on every multiple choice
[ ] Open-text option for "Why?" after key questions
[ ] No required questions (forced answers = bad data)
[ ] Mobile-friendly (50%+ will take it on phone)
```

### Sample Size Calculator

```
SAMPLE SIZE GUIDE
==================
Confidence level: 95% (standard)
Margin of error:  5% (standard)

Population size  | Sample needed
─────────────────┼──────────────
100              | 80
500              | 217
1,000            | 278
5,000            | 357
10,000           | 370
100,000+         | 384

REALITY CHECK: For early-stage discovery, 50-100 responses
with clear patterns is usually sufficient. Don't let perfect
sample sizes delay learning.
```

### Sean Ellis Question (built-in)

Always include this question for PMF measurement:

```
"How would you feel if you could no longer use [product]?"
  ○ Very disappointed
  ○ Somewhat disappointed
  ○ Not disappointed (it's not really useful)
  ○ N/A — I don't use [product]
```

### Output
Deliver: Complete survey with all questions + distribution plan + bias check + sample size target.

---

## Stage 3: Jobs-to-be-Done (`/discovery:jobs`)

**Goal:** Map what customers are actually trying to accomplish — the "job" they hire your product to do.

### JTBD Framework

```
JOBS-TO-BE-DONE MAP
=====================
CORE JOB STATEMENT:
  "When [situation], I want to [motivation], so I can [expected outcome]."

  Example:
  "When I'm preparing a board deck, I want to quickly pull accurate
  revenue metrics, so I can show investors we're on track."

FUNCTIONAL JOB (what they need to accomplish):
  ___

EMOTIONAL JOB (how they want to feel):
  ___

SOCIAL JOB (how they want to be perceived):
  ___
```

### Job Map (8 steps)

```
JOB MAP
========
Every job follows these steps. Find where the pain is worst.

Step              | What they do          | Pain level (1-5) | Current solution
──────────────────┼───────────────────────┼───────────────────┼─────────────────
1. Define         | Figure out what to do | /5                |
2. Locate         | Find inputs needed    | /5                |
3. Prepare        | Set up for the task   | /5                |
4. Confirm        | Verify readiness      | /5                |
5. Execute        | Do the core task      | /5                |
6. Monitor        | Track progress        | /5                |
7. Modify         | Make adjustments      | /5                |
8. Conclude       | Finish and evaluate   | /5                |

HIGHEST PAIN STEP: ___ (this is where your product should focus)
```

### Forces of Progress (Switch Analysis)

Why customers switch (or don't) from current solution:

```
FORCES OF PROGRESS
====================

PUSHING TOWARD CHANGE              RESISTING CHANGE
(reasons to switch)                (reasons to stay)

Push of situation:                 Allegiance to current:
"[Current pain/frustration]"       "[What they like about status quo]"
Strength: /5                       Strength: /5

Pull of new solution:              Anxiety of change:
"[What your product promises]"     "[What scares them about switching]"
Strength: /5                       Strength: /5

────────────────────────────────────────────────────
TOTAL PUSH: ___/10                 TOTAL RESIST: ___/10

If PUSH > RESIST: customers will switch (with the right trigger)
If RESIST > PUSH: you need to reduce anxiety or increase pain awareness
```

### Outcome Statements

```
DESIRED OUTCOMES
=================
For each important outcome, rate importance and satisfaction:

Outcome                              | Importance | Satisfaction | Opportunity
─────────────────────────────────────┼────────────┼──────────────┼───────────
"Minimize the time spent on [X]"     | /5         | /5           | ___
"Reduce the risk of [Y]"            | /5         | /5           | ___
"Increase the accuracy of [Z]"      | /5         | /5           | ___
"Eliminate the need for [W]"         | /5         | /5           | ___

OPPORTUNITY SCORE = Importance + (Importance - Satisfaction)
  If Importance=5, Satisfaction=2 → Opportunity = 5 + (5-2) = 8 (HIGH)
  If Importance=3, Satisfaction=4 → Opportunity = 3 + (3-4) = 2 (LOW)

Highest opportunity score = your biggest product opportunity.
```

### Output
Deliver: Core job statement + job map with pain scoring + forces of progress + outcome statements + highest-opportunity areas.

---

## Stage 4: Research Synthesis (`/discovery:analyze`)

**Goal:** Turn raw interview/survey data into actionable product and business insights.

### Synthesis Framework

```
RESEARCH SYNTHESIS
====================
Data collected:
  Interviews completed:     ___
  Survey responses:         ___
  Observation sessions:     ___

PATTERN IDENTIFICATION
  List every distinct insight, then count frequency:

  Insight                          | Frequency | Confidence
  ─────────────────────────────────┼───────────┼──────────
  [Pain point / behavior / need]   | ___/total | HIGH/MED/LOW
  [Pain point / behavior / need]   | ___/total | HIGH/MED/LOW
  [Pain point / behavior / need]   | ___/total | HIGH/MED/LOW

  HIGH confidence: 5+ mentions + consistent context
  MED confidence:  3-4 mentions or mixed context
  LOW confidence:  1-2 mentions, might be outlier
```

### Persona Synthesis

```
RESEARCH-BACKED PERSONA
=========================
Name:             [Archetype name, not a real name]
Role:             [Most common role in interviews]
Key quote:        "[Direct quote that captures their worldview]"

Goals:
  1. [Most mentioned goal]
  2. [Second most mentioned]

Frustrations:
  1. [Most mentioned pain]
  2. [Second most mentioned]

Current workflow:
  [Step-by-step of how they solve the problem today]

Trigger event:
  [What makes them start looking for a solution]

Decision criteria:
  1. [Most important factor in choosing a tool]
  2. [Second most important]

Willingness to pay: $___/mo (from survey or interview signals)
```

### Insight → Action Matrix

```
INSIGHT → ACTION MATRIX
==========================
Insight                    | Action             | Priority | Feeds into
───────────────────────────┼────────────────────┼──────────┼────────────
[Pain point confirmed]     | [Build/fix/change] | P1/P2/P3 | /gtm:positioning
[Unexpected behavior]      | [Investigate more] | P1/P2/P3 | /dt:define
[Pricing signal]           | [Adjust pricing]   | P1/P2/P3 | /gtm:pricing
[Feature request pattern]  | [Add to roadmap]   | P1/P2/P3 | Product backlog
[Segment with PMF]         | [Double down]      | P1/P2/P3 | /startup:pmf
```

### Research Quality Check

```
RESEARCH VALIDITY CHECK
=========================
[ ] Talked to actual ICP (not friends, not employees)
[ ] Mix of enthusiasts AND skeptics interviewed
[ ] Sample size sufficient for patterns (10+ for interviews)
[ ] Asked about behavior, not just opinions
[ ] Captured commitment signals (not just compliments)
[ ] Multiple data sources (interviews + survey, not just one)
[ ] Disconfirming evidence acknowledged (not just confirming)
[ ] Insights are specific enough to act on

Score: ___/8
If < 6: your research may be biased. Consider additional interviews
with a different demographic or more skeptical audience.
```

### Output
Deliver: Pattern analysis + research-backed persona + insight→action matrix + research quality score + specific recommendations.

---

## Integration Notes

- **Feeds into DT:** `/discovery:interview` results feed directly into `/dt:empathize` (personas, pain maps)
- **Feeds into GTM:** `/discovery:analyze` personas feed into `/gtm:positioning` (ICP definition)
- **Feeds into Startup:** `/discovery:jobs` outcome scores feed into `/startup:pmf` (what to measure)
- **Feeds into Pitch:** Customer quotes from interviews are gold for `/pitch:deck` Slide 2

## Principles

1. **Talk to users before writing code.** The cheapest way to validate is a conversation, not a prototype.
2. **Behavior over opinion.** What people DO tells you more than what they SAY they'd do.
3. **Compliments are not validation.** "That's cool" means nothing. "Can I pay you?" means everything.
4. **Small samples, strong patterns.** 10 interviews with clear patterns beat 1,000 survey responses with noise.
5. **The Mom Test is not optional.** If your mom would lie to be nice, your interview questions are wrong.
