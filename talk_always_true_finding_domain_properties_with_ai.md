# Always True: Finding Domain Properties with AI

_Length: 30 minutes_

Our tests on unit, API, and web UI level check the examples we thought of. The rules behind those examples stay unstated. General properties like "no visible or invisible crashes" catch some of what we missed, and they apply to any system. The valuable properties are the domain ones: things that are always true in *this* domain, whatever the input, whatever the path.

Finding them is a type of thinking humans turn out to be worse at than AI. We think in examples and stories; AI is comfortable proposing invariants. In this experience report from building agentic orchestration systems, AI reads the system under test and its implementation and proposes candidate properties: what seems to hold true. The team judges which should hold, and we turn those into tests on each level. Instead of asking AI to confirm what we meant, we ask it for the evidence against us. Properties we did not expect show where our expectations and the system part ways, and that is where attention should go.

You'll leave with a way to move your tests from examples to properties, and to tell the general properties apart from the domain properties that make your tests worth having.
