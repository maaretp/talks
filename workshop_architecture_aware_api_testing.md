# Architecture-aware Exploring of Programmatic Interfaces

_Length: 1/2 day_

_Target audience_: quality engineers working with APIs and method signatures

_Prerequisites_: technically inclined, unafraid of code

_Participants need_: Laptop with Bruno, a code editor, and a REST client or HTTP library in their language of choice

_Provided_: Practice API environment, examples in python

## Description

The API testing conversation is dominated by tool tutorials and automation frameworks. What is missing is the thinking layer - the architectural awareness and structured perspectives to learning while collecting information, that turn a capable technician into a tester that finds what matters. This workshop fills that gap through experiental learning and practice.

The core question with testing is results coverage - are we finding the problems there are to find? With modern architectures and API-thinking, our options for exploratory testing are greatly increased, but how do we do this systematically? APIs - or programmatic interfaces - can be found as the exposed ways of packaging our business logic but also on level of method signatures in unit testing. If 77% of production failures can be reproduced by a unit test, the architecture awareness allows us to shift down on our testing, exploring on APIs as well as units, increasing the opportunities of technical collaboration within our teams.

What participants leave with:

- a habit of asking "what's behind this endpoint?" while testing it
- a perspectives checklist they have already used to explore an API
- examples they can use as reference in their work

---

## Session plan

### Session 1: Code vs. Bruno vs. Schemathesis

Core question: Does your API exploration tool constrain or expand your testing?

How tooling shapes mental model:

- Bruno (collection-based, git-friendly exploration) — What does it mean to treat API exploration as a first-class, version-controlled artifact? How does working in a dedicated API client shape what you notice and what you overlook?
- Code (programmatic requests via scripts, libraries, or test frameworks) — When you write code to call an API, you gain precision and composability. But do you lose the serendipity of manual exploration?
- Schemathesis (properties of APIs to contract-first thinking) — Starting from the schema means starting from the promise. What does the API say it does, and how does that frame what you choose to test? What are properties common to all APIs?

Hands-on: Participants explore the same API using all three approaches in short rotations, then compare notes. What did each approach make easy to find? What did each approach make easy to miss?

Takeaway: There is no neutral tool. Each approach has an idea about what matters, and the aware tester picks deliberately.

### Session 2: Awareness of What's Behind the API

Core question: If you don't know the architecture, how do you know what to test?

This session makes the case that even a method is an API — any callable boundary is a surface worth understanding. We work through layers:

- The endpoint is a façade. What sits behind it? A direct database call? An orchestration layer coordinating five services? A queue that processes asynchronously? Each of these architectures produces a different failure profile.
- Methods are APIs too. The boundary between a caller and a callee is an interface with assumptions, contracts, and failure modes — whether it's an HTTP endpoint, a function signature, a message on a bus, or an event trigger. Testers who see this think in terms of boundaries, not just endpoints.
- Architecture patterns change risk. A synchronous call to a monolith fails differently than an async message through a broker. Caching layers hide staleness. API gateways apply policies you didn't write. Rate limiters, circuit breakers, and retry logic all live between your request and the thing that does the work.

Exercise: Given an architecture diagram of a realistic system, participants map where they would focus exploratory testing and why. Groups compare strategies and discover the perspectives they missed.

Takeaway: You cannot test an API effectively if you treat it as a black box by default. Informed exploration beats uninformed coverage.

### Session 3: The Perspectives Checklist

Core question: What should you always consider — and what do you keep forgetting?

This session introduces and pressure-tests a structured checklist of perspectives for API exploratory testing. The checklist is not a test plan — it's a set of lenses to look through before and during exploration.

Perspectives include:

- A thing that can be called can be called with just about anything. If an endpoint accepts input, someone will send it something you didn't expect. Malformed payloads, wrong types, empty bodies, enormous bodies, unexpected encodings, duplicate parameters — the call surface is the attack surface.
- Security controls have API impact. Authentication, authorization, rate limiting, input validation, CORS policies, token expiry — these aren't just security concerns. They shape what the API does and doesn't allow, and they interact with functional behavior in ways that surprise people. A tester who ignores security controls is testing a version of the API that doesn't exist in production.
- State and sequence matter. APIs aren't stateless just because HTTP is. What happens when you call things out of order? What happens when you call the same thing twice? What about concurrent calls that compete for the same resource?
- Error responses are a feature. What does the API tell you when things go wrong? Too much information leaks implementation details. Too little leaves callers guessing. Inconsistent error shapes break clients.
- Contracts drift. The documentation says one thing, the schema says another, and the implementation does a third. Testing the gaps between these is some of the highest-value work a tester can do.
- Environment and configuration shift behavior. The same API in dev, staging, and production may behave differently because of feature flags, data volumes, downstream dependencies, or infrastructure configuration.
- Observability is testable. Does the API produce the logs, metrics, and traces that someone will need when debugging at 2 AM? If you can't observe it, you can't operate it.

Hands-on: Participants apply the checklist to a live API, working in pairs. Each pair picks two perspectives to explore deeply, then presents their findings to the group. The goal is not coverage — it's demonstrating how a perspective shift changes what you find.

Takeaway: The checklist as a printed/digital reference, plus the experience of having used it under real conditions.
