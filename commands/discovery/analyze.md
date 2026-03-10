---
name: discovery analyze
description: Synthesize interview and survey data into actionable insights
---

Run the Research Synthesis exercise from `~/.claude/skills/discovery/SKILL.md` (Stage 4: Research Synthesis).

1. Ask the user to paste or describe their research data (interview notes, survey results, observation logs)
2. Identify patterns with frequency counts and confidence levels (HIGH/MED/LOW)
3. Build a research-backed persona from the data:
   - Archetype name, role, key quote
   - Goals, frustrations, current workflow
   - Trigger event, decision criteria, willingness to pay
4. Generate the Insight-to-Action matrix:
   - Each insight mapped to a concrete action, priority (P1/P2/P3), and downstream skill
5. Run the research quality check (score out of 8)
6. If quality score < 6, recommend specific next steps to strengthen the research

Cross-references: insights feed into `/gtm:positioning` (ICP), `/dt:empathize` (personas), `/startup:pmf` (what to measure), `/pitch:deck` (customer quotes).

Output format: Pattern analysis + persona + insight-action matrix + quality score + recommendations.
