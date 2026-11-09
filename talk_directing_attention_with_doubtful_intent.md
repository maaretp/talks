# Directing Attention with Doubtful Intent

_Length: 30 or 45 minutes_

Quality engineering is not a phase after development. It is the search for team practices that bridge us, so that what we intend, what we build, and what we learn turn into delivered value instead of handoffs. AI made that search more urgent by making artifacts cheap to produce.

Developers rarely experience their work as delivering to a specification. We experience it as solving problems. Building an agentic orchestration system, we received 80 pages of generated specification: well-structured, confident, and empty. It did not address the questions we actually ran into while building. On another project, eight months of specification fed two sprints of AI-native development. Different projects, same pattern: documents stood between the people who needed to collaborate, and every handoff between phases produced more waste than understanding.

This experience report shares two quality engineering practices that bridged the gap. Both rest on doubtful intent: instead of asking AI to confirm what we meant, we ask it to show us where we might be wrong.

- **Living common ground bridges people.** We stopped handing over specifications and started ingesting conversations. Discussions, decisions, and open questions go into an LLM-maintained wiki that both people and agents read from. The same source directs the team's understanding and the agents' context, and it changes as we learn. The specification becomes a by-product of solving problems together, not an input passed between roles.
- **Properties bridge intent and implementation.** Our tests on unit, API, and web UI level checked the examples we thought of. General properties like "no visible or invisible crashes" catch some of what we missed. The valuable ones are domain properties: things that are always true in *this* domain. Finding them is a type of thinking humans turn out to be worse at than AI. AI proposes candidates from the system under test and its implementation, the team judges which should hold, and the tests keep checking them. Properties we did not expect show where the system and our expectations part ways.

The two work at opposite ends: common ground grows from what we intend, properties from what we built. Neither belongs to a tester or a phase; both are things the whole team does, developers included. You'll leave with two team practices to try, and a quality engineering view of collaboration where doubt directs attention to where value is at risk.
