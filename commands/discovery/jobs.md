---
name: discovery jobs
description: Jobs-to-be-Done mapping and switch analysis
---

Run the Jobs-to-be-Done exercise from `~/.claude/skills/discovery/SKILL.md` (Stage 3: Jobs-to-be-Done).

1. Ask what product/service the user is building and what problem it solves
2. Draft the core job statement: "When [situation], I want to [motivation], so I can [expected outcome]"
3. Break the job into functional, emotional, and social dimensions
4. Walk through the 8-step Job Map, scoring pain at each step (1-5)
5. Build the Forces of Progress diagram (push vs resist)
6. Generate outcome statements with opportunity scores (Importance + gap)
7. Identify the highest-opportunity area — where the product should focus

If the user provides interview data or notes, incorporate real quotes and patterns. Otherwise, generate a hypothesis-driven map they can validate through interviews (`/discovery:interview`).

Output format: Complete JTBD map with job statement, job map, forces diagram, and ranked opportunity scores.
