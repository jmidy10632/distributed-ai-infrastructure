# Questions I Hope Reviewers Will Help Answer

Version 0.1 is meant to be questioned. These are the areas where I believe the paper most needs outside knowledge, measurements, and honest disagreement.

You do not need to review the whole paper. Taking one claim seriously, finding its best evidence, and explaining what it does or does not support would be genuinely helpful.

Review from outside the United States is especially important. The current draft uses several United States sources because they were available during the first research pass, not because one country's grid, climate, laws, costs, or public process represents the world.

## How much usable capacity is really available?

Connected devices are numerous, but that does not make all of their computing power available. How much useful capacity remains after accounting for ownership, availability, memory, bandwidth, security, reliability, and energy efficiency?

Measurements of real device inventories, utilization, hardware capabilities, and willingness to participate would help answer this.

## How should the environmental comparison be made?

What would constitute a fair electricity, water, land, hardware, and emissions comparison between centralized and distributed execution?

The comparison needs to include network energy, cooling, utilization, embodied hardware impacts, and local grid conditions. Annual averages alone may hide the effects that matter most.

## Can work on unfamiliar hardware be trusted?

Which combinations of attestation, isolation, encryption, replication, and result checking are practical across different kinds of devices?

Useful contributions would include threat models, performance costs, compromise tests, and a clear explanation of where hardware roots of trust fall short.

## Can an enterprise keep control of its data?

How would an organization enforce data residency, retention, model licensing, audit, and incident-response requirements across a trusted federation?

I am especially interested in failure cases: what happens when a participant leaves, a key is compromised, a deletion request cannot be confirmed, or two jurisdictions impose conflicting requirements?

## Which workloads actually benefit?

Which workloads gain a measurable advantage from being distributed, and which should remain centralized?

A good benchmark would compare output quality, latency, throughput, cost, energy, security, and operational complexity instead of choosing only the metric that favors one design.

## How can participation avoid creating another gatekeeper?

What governance or compensation model would support voluntary participation without concentrating control in a new intermediary?

Cooperative, federated, commercial, and public-interest approaches are all worth examining. So are the ways each model could be abused or gradually centralized.

## How should local limits affect placement?

How should local grid capacity, water, noise, land, property, and community effects influence where a workload runs?

The answer needs measurable thresholds and accountability, not simply a promise to consider local conditions.

## What is the smallest test worth running?

What is the smallest proof of concept that could test the central idea and produce a result other people can reproduce?

It should have a bounded workload, a centralized comparison, a known hardware inventory, a threat model, a measurement plan, and clear failure criteria.

## How does the answer change from place to place?

How does feasibility change across regions with different energy systems, grid reliability, water stress, climates, connectivity, device ownership, costs, laws, and institutions?

The project needs evidence from a range of countries and communities. A design that works well in one place may be inefficient, unaffordable, insecure, or impractical somewhere else.

## The question that has to remain open

Under what conditions is decentralization worse than a modern data center?

If the project cannot answer that question honestly, it will not produce a useful decision framework.
