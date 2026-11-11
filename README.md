# Distributed Artificial Intelligence Infrastructure

- **Author:** John D. Midyette
- **Current version:** 0.1 working draft
- **Status:** Open for criticism and collaboration
- **Political position:** Neutral
- **Geographic scope:** Global

## Why I started this project

I came to this idea by paying attention to what was happening around artificial intelligence and the infrastructure being built to support it. Demand for computing was rising quickly, increasingly large data centers were being proposed, and communities were being asked to absorb the consequences: new pressure on electrical grids and water supplies, additional transmission infrastructure, land use changes, noise, and long-term commitments of local resources.

At the same time, I could see another part of the picture. Computing capacity is already distributed throughout the world in personal devices, businesses, universities, laboratories, telecommunications networks, and smaller regional facilities. Open-source models were becoming more capable, more efficient, and easier to run on modest hardware. That led me to a basic question: before building every new workload around another large centralized facility, should we first determine how much useful capacity already exists and how responsibly it could be coordinated?

I am not suggesting that every data center is unnecessary or that distributed computing will solve every problem. Some workloads genuinely require specialized, tightly connected infrastructure. But the choice should not automatically be between building another hyperscale facility and going without the technology. There should be room for another approach - one that matches each workload to the smallest, nearest, most efficient, and most accountable resource capable of handling it.

That is where this project began. I saw a need for a credible alternative and believed the idea was important enough to put forward for examination. This working paper is not presented as a finished answer. It is an invitation to test the premise, challenge the assumptions, identify the limits, and determine whether a more distributed model can become a practical part of the world's computing infrastructure.

## The idea

The paper explores an open distributed compute fabric that could use suitable capacity already present in personal devices, businesses, universities, laboratories, telecommunications networks, and smaller regional facilities.

The guiding thought is simple:

> Put each workload on the smallest, nearest, most efficient, and most accountable resource that can perform it safely and reliably.

That will not work for every workload. Frontier training and other tightly coupled jobs may continue to require specialized centralized facilities. The question is whether smaller models, private inference, retrieval, batch processing, federated learning, and other divisible work can be handled differently.

## Long-term goal

The long-term goal is to develop an open, interoperable standard and a complete open-source reference framework for coordinating distributed artificial intelligence workloads across independently controlled computing resources. The intended result is not just a paper. It is a practical body of specifications, reference code, conformance tests, and operational guidance that others can implement, examine, and improve.

The current repository does not claim that this standard or framework already exists. Reaching that point will require public review, measurable experiments, reproducible implementations, independent security analysis, transparent governance, and contributions from multiple disciplines and regions. Any standard should emerge from evidence and working code rather than being declared in advance by one person or organization.

## Stewardship and collaboration

This project began with an individual observation and a working proposal, but its scope is larger than any one person's experience or capacity. I am serving as the project's initiator and initial editor, not as its sole technical authority. My responsibility at this stage is to put the idea forward clearly, keep the record honest, and create a place where its assumptions can be tested.

The project is actively seeking critical reviewers, domain specialists, contributors, and prospective maintainers. Useful participation includes identifying weaknesses, contributing evidence, proposing competing approaches, testing technical claims, and helping determine whether a practical decentralized framework can be developed. No one needs to agree with the paper's premise in order to make a valuable contribution.

The long-term success of this work should not depend on one person. If a sustained contributor community develops, stewardship and decision-making should be shared among people who have demonstrated sound judgment, technical care, respectful conduct, and a commitment to the project's neutral and evidence-based purpose.

## Political neutrality

This project is politically neutral. It does not endorse a party, candidate, campaign, or ideology.

Election results, permitting decisions, project withdrawals, and public opposition can be relevant evidence, but only when they are tied to a particular place, date, decision, and source. The same standard applies whether the evidence supports or challenges the paper.

The complete statement is in [POLITICAL_NEUTRALITY.md](POLITICAL_NEUTRALITY.md).

## Geographic neutrality

This is a global question, and no country or region is treated as the default. The paper currently uses several United States sources and examples, but they are examples rather than a stand-in for the world.

The practicality of distributed computing will change with local energy systems, grid reliability, climate, water availability, connectivity, device ownership, costs, laws, institutions, and community priorities. Evidence from any region is welcome, and conclusions should remain tied to the places where the evidence applies.

The complete statement is in [GEOGRAPHIC_NEUTRALITY.md](GEOGRAPHIC_NEUTRALITY.md).

## What I am not claiming

I am not claiming that distributed devices can replace every data center, that decentralization is automatically more sustainable, or that the theoretical capacity of millions of devices is the same as usable capacity.

I am also not claiming that every canceled or opposed project failed for the same reason. Those outcomes need to be examined one at a time. If the evidence does not support a claim in the paper, the claim should be narrowed or removed.

## Reading and taking part

- [Working paper](WHITEPAPER.md)
- [Open questions](REVIEW.md)
- [Evidence still being checked](EVIDENCE_LEDGER.md)
- [Data-center project outcomes](OUTCOME_REGISTRY.md)
- [How to contribute](CONTRIBUTING.md)
- [Geographic neutrality](GEOGRAPHIC_NEUTRALITY.md)
- [How the project is maintained](GOVERNANCE.md)
- [Where the work could go next](ROADMAP.md)
- [Version history](CHANGELOG.md)

The current [Word review copy](releases/whitepaper-working-draft-v0.1-long-term-goal.docx) is available in the releases directory.

GitHub Discussions are the best place for broad criticism, competing ideas, and questions. Issues are useful for a specific factual problem or missing source. Pull requests are welcome when someone has a concrete revision to propose.

Criticism is not a problem to be managed here. It is part of the work. Evidence that favors centralized infrastructure, shows a distributed approach performing poorly, or disproves an assumption is just as valuable as evidence supporting the proposal.

## Sources

Whenever possible, claims should point to original records, reproducible research, or clearly documented measurements. Forecasts should remain forecasts, assumptions should be identified as assumptions, and uncertainty should remain visible.

The paper and repository text are available under the [Creative Commons Attribution 4.0 International License](LICENSE). Citation information is in [CITATION.cff](CITATION.cff).
