# Directing Attention with Doubtful Intent

_Length: 30 or 45 minutes_

Requirements are hypotheses: incomplete, sometimes contradictory, often wrong. Yet we still pass them from role to role as if they were raw material. On one project, eight months of specification fed two sprints of development. Doubtful intent is a different way of asking. Instead of asking AI to confirm what we meant, we ask it for the evidence against us and let that evidence decide where attention goes.

In this talk, I share two practices we tried, one at each end of the work: specification and testing. Each is aimed at a problem we kept running into without it:

- **Living common ground.** *Without it*, specification is a handoff: written apart from the people who build, and out of date by the time it arrives. *With it*, specification enters through the team's conversations and writing and builds a shared knowledge base with role-specific views, traceable changes, and a path from text to executable specification. Developers specify as they solve. Scope stays put while understanding grows.
- **System properties.** *Without them*, our tests cover the examples we thought of, and the rules behind them stay unstated. *With them*, AI proposes candidate properties, a model of what should hold true in the domain. The team judges which matter, and we check the built system against them. Mismatches show where expectations and behavior part ways.

Both follow the same pattern: generate, surface, reconcile. You'll leave with two ways to ask AI for the evidence against you, and to let doubt show you where to look.
