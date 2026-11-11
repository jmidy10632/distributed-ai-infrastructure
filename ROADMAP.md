# Where This Could Go

This is a direction rather than a fixed schedule. The next version should be shaped by what reviewers find, including evidence that the idea needs to be narrowed or abandoned in some areas.

## Long-term objective

The long-term goal is to develop an open, interoperable standard and a complete open-source reference framework for coordinating distributed artificial intelligence workloads. A useful result would include specifications, working reference code, conformance tests, security and operational guidance, and documented methods for measuring performance and environmental effects.

That outcome cannot be established by this paper or by one implementation. It would require public review, measurable experiments, reproducible results, independent security analysis, transparent governance, and contributions from multiple disciplines and regions. The standard should follow evidence and working code rather than getting ahead of them.

## First: check the paper

The immediate work is to verify every important source, correct unsupported claims, collect serious counterarguments, and improve the open questions. The project-outcome registry should grow only from records that can be checked.

## Then: define requirements and boundaries

If the premise survives review, contributors should define the workloads the system is intended to support, the workloads it should reject, and the minimum requirements for identity, security, privacy, reliability, energy accounting, data control, and interoperability. These requirements should remain neutral about vendors, regions, and particular implementations.

## Next: define a fair test

A small pilot should compare a centralized and distributed approach using the same workload and quality target. The comparison should include cost, latency, throughput, energy, network overhead, security, and operational effort.

The methods and failure criteria should be published before the results. A negative result is still a useful result.

## Build a minimum reference implementation

The first code should test the smallest useful path through the proposed architecture: describe available capacity, submit a bounded workload, match it to an eligible node, protect the data, verify execution, return the result, and record the relevant measurements. It should favor clear interfaces and replaceable components over premature scale.

## Run, reproduce, and improve

The first pilot should not be treated as a verdict. Other people should be able to reproduce it, challenge the assumptions, and test different hardware or locations. The paper should change when the results require it.

## Develop interoperability and conformance

Once more than one implementation can perform the same bounded work, the project can begin defining portable interfaces, capability descriptions, identity and attestation formats, workload packaging, telemetry, accounting, and result verification. Conformance tests should show whether independently developed components can work together without relying on one coordinator or vendor.

## Establish durable governance

A credible standard will need a documented process for proposing changes, recording objections, resolving security issues, maintaining compatibility, and preventing any contributor or organization from treating the project as proprietary infrastructure. Governance should evolve with actual participation rather than being designed around contributors who have not yet arrived. Before accepting substantial code, the project should also document a software license, contribution terms, and patent expectations separately from the paper's text license.

## Before calling anything final

A version 1.0 would need independently checked evidence, a clear record of unresolved objections, reproducible pilots, a usable reference implementation, documented security review, conformance tests, and claims limited to what was actually measured. If the evidence shows that part of the proposed approach is infeasible, that result should narrow the standard rather than be concealed.
