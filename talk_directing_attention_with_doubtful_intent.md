# Directing Attention with Doubtful Intent

*Length: 30 or 45 minutes*

Eight months of specification for two sprints of development shows a new failure mode: a handoff-based way of working fails at value delivery. Removing handoffs needs a different kind of asking: doubtful intent. It is grounded in Dijkstra's age-old wisdom: you can't prove that it works, but every honest failed attempt to show it doesn't brings you closer to a practical proof.

In this talk, I share three experiments in directing attention with doubtful intent, where developers specify as they solve and testing samples to surface what deserves attention:

- Living common ground. A knowledge base that grows from what we say and write: one shared core, a view for each role, every change traced, and text that turns executable over time.
- Property-based testing. LLMs propose rules that humans struggle to state, and humans judge them where sampled examples fail.
- Model reconciliation. AI generates models of the system, and the gaps between those models and our expectations show where to look.

Ask AI for the evidence against you, and let doubt show you where to look.

---


We can now do things by *asking for it*: our intent matters. 
Generate, Surface, Reconcile
“You can’t prove correctness”. You need to use AI to surface disagreement and incorrectness.  Attention is expensive and needs support in things that aren't "dev". 

I have experimented in asking for three things that come from a doubtful intent in need of support: 

- Living common ground.  A knowledge base that grows from what we say and write: one shared core, a view for each role, every change traced, and text that turns executable over time.
- Property-based testing. LLMs propose rules that humans struggle to state, and humans judge them where sampled examples fail.
- Model reconciliation. AI generates models of the system, and the gaps between those models and our expectations show where to look. 

Doubtful intent is that whatever was specified follows ideas like "Requirements aren't raw materials. They're hypotheses, often incomplete, contradictory, and frequently wrong." and that we need help in noticing things that are off by naming things that could be off, and reconciliating those perspectives.

We already hear reports where spec took 8 months, and dev took 2 sprints, making the core of dev more efficient with AI. 

We need to have teams where spec, dev and test are folded into an engineering team. 


Everything is uncertain, everything uncertain is a hypothesis.
Requirements are hypotheses, often incomplete, contradictory and frequently wrong
Our isolation of dev from spec and test is a hypothesis I already investigated: Our hypothesis was that a customer-obsessed team in direct contact with its customers would do better without a proxy. We did much better with less focus on specification, and that would make a great foundation for AI enabled teams.
I experiment with practices now that come from a doubtful intent, and I want to tell about those in this talk.

Point 0: No product owner Our hypothesis was that a customer-obsessed team in direct contact with its customers would do better without a proxy. Developers owned the product they were building. They took features from problems no one had asked them to solve, used telemetry to learn, and released continuously. The team delivered more, and the way of working survived a reorg. Skeptics said one team wasn’t proof, and that most teams lack the seniority and communication skills to try it.AI changes that objection. Spec, dev and test are still silos, and automating one silo doesn’t automate delivery. It just moves the queue to the next handoff.

Point 1: Fully automated, deeply human. If 10 people in team creates 45 connections between individuals to maintain, less people is needed to move fast and keep people informed. When significant chunks of conversations are with AI into the artifacts including the system, we need to build a shared sociotechnical system. 

Point 2: Isolating spec -> code -> testing may make the first fast but the two others extremely slow and wasteful. Folding them into engineering together becomes essential. 

Point 3: I have three concrete experiments around attention techniques to report on. 
