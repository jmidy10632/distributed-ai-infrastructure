# Distributed Artificial Intelligence Infrastructure

**A Decentralized Alternative to Concentrated Data Center Development**

**John D. Midyette**

**WORKING DRAFT FOR DISCUSSION AND COLLABORATION**

VERSION 0.1  |  NOVEMBER 2026

# Document Status

This working draft presents an exploratory framework for decentralized artificial intelligence infrastructure. It is being circulated for review to identify unsupported assumptions, improve the proposed architecture, and evaluate its environmental, security, economic, and operational feasibility. Its claims and design proposals remain subject to revision.

This project is politically neutral. It does not endorse or oppose any political party, candidate, or ideology. Elections, permitting decisions, project withdrawals, and public opposition are considered only as verifiable evidence about infrastructure feasibility, public acceptance, and local effects. Identical evidence standards apply regardless of who supports or opposes a project.

This project is also geographically neutral. No country, region, grid, climate, market, or legal system is treated as the default. United States data and project examples in this draft are illustrative rather than globally representative. The feasibility and effects of distributed infrastructure must be evaluated under the local energy mix, grid conditions, water availability, connectivity, device ownership, costs, laws, institutions, and community priorities of each place.

This draft does not present a completed system or claim that distributed devices can replace every data center. It proposes a direction for investigation, with an initial emphasis on practical inference, specialized models, federated learning, and divisible workloads. Environmental benefits must be measured, and centralized infrastructure remains appropriate where technical requirements justify it.

# Author's Note

I came to this idea by watching demand for artificial intelligence grow alongside proposals for increasingly large data centers. Communities were being asked to absorb new pressure on electrical grids and water supplies, additional transmission infrastructure, land use changes, noise, and long-term commitments of local resources.

At the same time, computing capacity was already distributed across personal devices, businesses, universities, laboratories, telecommunications networks, and smaller regional facilities, while open-source models were becoming more capable and efficient. That raised a basic question: before directing every new workload to another large centralized facility, should we first determine how much useful capacity already exists and how responsibly it could be coordinated?

This paper grew from that question. It does not claim that every data center is unnecessary or that distributed computing is appropriate for every workload. It puts forward an alternative for examination and invites others to challenge the assumptions, identify the limits, and help determine where a more distributed model is practical.

# Abstract

Artificial intelligence is commonly treated as inseparable from the construction of increasingly large data centers. That assumption should be reconsidered. Centralized facilities remain appropriate for frontier model training and other workloads that require tightly coupled accelerators. Some practical artificial intelligence workloads can nevertheless be performed by smaller models running on distributed hardware.

Opposition to data center development has become a material infrastructure constraint. Communities have objected to projects because of electricity and water requirements, noise, air emissions, land use changes, transmission construction, utility costs, and the proximity of industrial facilities to homes. Numerous projects have consequently been withdrawn, denied, delayed, relocated, or reduced in scale. These outcomes show that the costs and benefits of concentrated computing are often distributed unevenly.

This paper proposes an open distributed compute fabric that coordinates computers already present in businesses, institutions, homes, laboratories, telecommunications networks, and regional facilities. The objective is to place each workload on the smallest, nearest, lowest impact resource capable of executing it securely and reliably. Open source models, local first execution, energy aware scheduling, hardware attestation, encrypted communication, and voluntary participation may reduce unnecessary dependence on new hyperscale facilities while improving organizational control over data and operations. These benefits require validation through measurement and limited pilots.

The long-term goal is to develop an open, interoperable standard and a complete open-source reference framework for coordinating distributed artificial intelligence workloads. Reaching that goal will require public review, measurable experiments, reproducible implementations, independent security analysis, transparent governance, and contributions from multiple disciplines and regions.

# 1. The Infrastructure Question

Demand for artificial intelligence computation is growing more rapidly than the infrastructure historically used to supply it. Lawrence Berkeley National Laboratory estimates that data centers could account for approximately 11.8 percent of United States electricity consumption by 2030, with modeled scenarios ranging from 9.5 to 15.3 percent. The corresponding estimate is between 521 and 843 terawatt hours annually. These figures are forecasts rather than guarantees, but their scale makes data center expansion an electricity system, land use, water management, and community planning issue.[1]

The practical limitation is not simply the amount of electricity generated over an entire year. A data center requires sufficient power at a specific location, through specific transmission lines, substations, transformers, and distribution equipment, at the time the facility expects to operate. Generation located elsewhere does not solve a local capacity constraint unless the required transmission capability also exists.

In its 2026 draft National Transmission Needs Study, the Department of Energy identified a pressing need for additional transmission infrastructure due in part to load growth from data centers and other large industrial users. The North American Electric Reliability Corporation has also identified rapidly growing computational loads as a reliability and planning concern.[2][3]

The electric grid is not uniformly incapable of supporting additional data centers. It is also not reasonable to assume that every proposed facility can be supported in every proposed location on the schedule sought by its developer. New generation, high voltage transmission, substations, and large transformers often require substantially more time to plan and build than computing campuses.

**Table 1 Infrastructure Constraints**

| Constraint | Planning Issue | Implication |
| --- | --- | --- |
| Electricity | Capacity must be available at the proposed site and operating time | Annual generation totals do not establish local readiness |
| Transmission | New lines and substations can require long permitting and construction periods | Compute deployment can outpace grid expansion |
| Water | Cooling and electricity generation can affect constrained watersheds | Site conditions matter more than a national average |
| Community acceptance | Noise, land use, utility costs, and nearby infrastructure affect residents | Approval cannot be treated as a routine communications task |

# 2. Public Opposition as Infrastructure Evidence

Public opposition to data center projects is sometimes described as resistance to technological progress. That description overlooks the substance of many objections. Residents may be asked to accept an industrial facility that consumes hundreds of megawatts, requires new utility infrastructure, operates continuously, changes nearby land, produces mechanical noise, and uses local water or wastewater capacity. The artificial intelligence services and economic benefits may be delivered primarily to customers located elsewhere.

Under those conditions, opposition can reflect a reasonable assessment that local costs have not been fully disclosed, mitigated, or balanced by durable local benefits. Communities are entitled to ask who receives the benefits, who bears the risks, and what happens if resource projections or operating assumptions prove inaccurate.

No single authoritative registry captures every canceled or opposed data center development. Available research nevertheless shows a clear pattern. An Electric Power Research Institute community-centered study cited a Heatmap Pro review reporting that at least 25 United States projects were canceled due to local opposition in 2025, compared with six in 2024 and two in 2023.[4]

Representative cases include a proposed 14 billion dollar development in Arizona that was withdrawn following opposition concerning noise, building scale, and local resources; a proposed 1.3 billion dollar campus in Chesterton, Indiana, that was withdrawn after residents raised concerns involving air, water, electricity, wetlands, wildlife, and property values; and a facility proposed for Monterey Park, California, that was withdrawn after sustained opposition and a local moratorium.[5][6][7]

Some withdrawn projects return in smaller form or move to another location. That does not invalidate the pattern. It shows that public opposition changes project scale, siting, conditions, and feasibility. If the same infrastructure model repeatedly encounters opposition across unrelated communities, the appropriate response is to examine the architecture as well as the approval process.

# 3. Environmental and Community Constraints

## 3.1. Electricity

The environmental cost of computation depends on more than server efficiency. It also depends on the electricity source, time of operation, transmission losses, cooling requirements, server utilization, and infrastructure constructed to serve the load. A highly efficient facility can still create substantial absolute demand when its scale grows faster than its efficiency improves.

Large computational loads can also change electricity demand rapidly. Grid planners must account for both the amount of electricity consumed and the electrical behavior of the facility. Additional generation, storage, transmission, or demand management may be required to maintain reliability.

## 3.2. Water

Data centers may consume water directly through cooling and indirectly through electricity generation. The amount varies according to climate, cooling design, electrical supply, server efficiency, utilization, and time of operation. Berkeley Lab researchers found that workload level water consumption can vary by more than four orders of magnitude across different infrastructure and operating conditions.[8]

There is therefore no responsible universal claim that all data centers have the same water footprint or that one cooling method eliminates the issue everywhere. In water stressed areas, even an efficient facility can compete with residential, agricultural, industrial, or ecological uses. The relevant question is whether the proposed use is compatible with local conditions over the full operating life of the facility.

## 3.3. Air Quality, Noise, and Land

Data centers commonly use stationary engines or turbines for primary or backup power. These sources are regulated because combustion can produce nitrogen oxides, particulate matter, and hazardous air pollutants. Backup systems may operate during outages, testing, maintenance, or periods when grid service is constrained.[9]

Cooling equipment, transformers, generators, and electrical infrastructure may also produce continuous or intermittent noise. The effect is site specific, but proximity to residences makes it a legitimate engineering and siting consideration.

Land impacts extend beyond the data center parcel. A campus may require new substations, transmission corridors, access roads, pipelines, or generation facilities. In the United States, transmission development can involve negotiated easements and, under defined legal processes, court ordered eminent domain. This authority generally belongs to qualifying infrastructure entities rather than the data center operator, but the practical effect on a landowner can be the same.[10]

## 3.4. The Sustainability Test

An infrastructure model is not sustainable if each expansion requires increasingly difficult transfers of water, electricity, land, and environmental burden from service users to communities with limited influence over that service. This does not mean that no new data center should be constructed. It means that construction should occur where the total benefits justify the full costs and should not be the automatic response to every increase in compute demand.

# 4. Compute as a Distributed Resource

Computing capacity already exists across desktop computers, workstations, laptops, smartphones, enterprise servers, private clusters, universities, telecommunications networks, industrial systems, and smaller regional facilities. Many of these devices now include graphics processors or neural processing units that can execute useful artificial intelligence workloads at comparatively low power.

The International Telecommunication Union estimated 9.5 billion mobile cellular subscriptions worldwide in 2026 and approximately 6.3 billion people using the Internet. Subscription totals are not equivalent to available artificial intelligence nodes, but they demonstrate the physical distribution of connected electronics.[11]

A single consumer device is not a substitute for a tightly interconnected accelerator cluster. Aggregate theoretical performance is also not the same as usable capacity. Devices differ in memory, bandwidth, instruction support, availability, ownership, security, cooling, and energy efficiency.

The distributed ecosystem nevertheless represents a significant resource for workloads that can run locally, divide into independent tasks, use smaller or quantized models, tolerate opportunistic scheduling, or move to another node when a device becomes unavailable. Research into collaborative edge inference has demonstrated that neural network workloads can be partitioned across heterogeneous devices.[12]

# 5. Open Distributed Compute Fabric

The proposed alternative is an Open Distributed Compute Fabric. It is a standards based system that coordinates independently controlled computing resources without requiring owners to surrender permanent control of their hardware or data. The fabric would route work across four resource tiers.

**Table 2 Resource Tiers**

| Tier | Resource | Typical Work | Control Model |
| --- | --- | --- | --- |
| 1 | Local devices | Transcription, classification, personal assistance, image processing | Device owner retains data and execution control |
| 2 | Premises infrastructure | Retrieval, code analysis, private inference, parameter efficient tuning | Organization controls equipment and policies |
| 3 | Trusted federations | Shared batch inference, research, federated learning | Members operate under common security and accounting rules |
| 4 | Regional capacity | Larger models and specialized hardware requirements | Regional providers supply capacity under portable standards |

The purpose of this hierarchy is not to eliminate every data center. It is to prevent small and medium workloads from defaulting to hyperscale infrastructure when a closer and lower impact resource can satisfy the requirement.

# 6. Operating Principles

**Local first  **Work should execute where its data originates when local hardware can meet the required performance, security, and energy limits.

**Smallest capable model  **The fabric should choose the smallest model that meets a defined quality threshold. Quantization, distillation, sparsity, retrieval, and caching can reduce compute requirements.

**Data minimization  **Raw corporate or personal data should not leave its controlling environment merely because a remote model is convenient. Distributed jobs should receive only the information needed for their assigned task.

**Energy aware scheduling  **Nodes should publish power limits and operating conditions. Schedulers should consider device efficiency, grid conditions, battery status, cooling requirements, and available renewable generation.

**Voluntary participation  **Resource owners should decide which equipment participates, which workloads may run, and when capacity is available.

**Verifiable execution  **Signed software, reproducible environments, remote attestation, redundant execution, and result comparison should be available when a compute provider is not fully trusted.

**Open interoperability  **Models, containers, identities, telemetry, and accounting should use documented interfaces so that no single coordinator becomes a new point of dependence.

# 7. Workload Placement

A credible decentralized system must identify which workloads can move responsibly and which still require specialized centralized infrastructure.

**Table 3 Workload Suitability**

| Strong Initial Candidates | Limited or Unsuitable Candidates |
| --- | --- |
| Private document retrieval and summarization | Frontier model pretraining with tightly coupled accelerators |
| Batch classification and data extraction | Workloads with extremely high inter node communication |
| Speech recognition and translation | Strict real time services over unpredictable public nodes |
| Embedding generation and domain specific inference | Jobs requiring memory available only on specialized hardware |
| Parameter efficient tuning and federated learning | Safety critical functions without deterministic verification |
| Scientific parameter sweeps and rendering | Sensitive work on untrusted hardware without adequate isolation |

# 8. Environmental Requirements for Decentralization

Decentralization is not automatically sustainable. Poorly coordinated consumer hardware can be less efficient than a modern data center. A network of older machines running continuously could increase total electricity consumption. The environmental case must therefore be measured rather than assumed.

1. Use already deployed equipment before commissioning new equipment.

1. Run shared workloads only on nodes that meet minimum performance per watt thresholds.

1. Do not consume personal device batteries for nonessential shared work.

1. Prefer local execution when network transfer would dominate energy use.

1. Schedule flexible jobs during periods of lower grid demand and available clean generation.

1. Measure marginal electricity and water effects instead of relying only on annual averages.

1. Account for embodied hardware impacts and the benefits of extending useful equipment life.

1. Prevent local concentrations of distributed nodes from recreating a data center without equivalent review.

1. Publish auditable utilization and environmental metrics.

1. Stop or relocate work when local infrastructure approaches defined limits.

# 9. Organizational Value

A decentralized architecture can give businesses more control over intellectual property, regulated information, source code, customer records, and confidential documents. Open source models can run on equipment owned by the organization or within a federation whose operating policies the organization accepts.

This arrangement can reduce the number of third parties receiving sensitive data and limit uncertainty involving retention, secondary use, training, jurisdiction, and administrative access. It can also reduce dependence on a single application programming interface, pricing model, cloud region, or proprietary model.

Decentralization does not eliminate governance work. Organizations still require access control, patching, model evaluation, monitoring, incident response, license management, and audit records. It can replace some recurring third party transfer reviews with a clearer technical rule: approved computation goes to the data, while the data remains inside an environment controlled by the organization.

# 10. Implementation Path

## 10.1. Enterprise Pilot

- Inventory existing central processors, graphics processors, neural processors, and server capacity.

- Select two or three bounded inference workloads with measurable quality requirements.

- Deploy signed and containerized open source models inside the organization.

- Measure cost, power, latency, utilization, security events, and output quality.

## 10.2. Trusted Institutional Federation

- Connect several organizations under a common policy framework.

- Introduce workload portability, hardware attestation, and geographic controls.

- Test failure recovery, accounting, result verification, and data deletion.

## 10.3. Regional Compute Exchange

- Add universities, laboratories, smaller data centers, and community owned resources.

- Implement energy aware scheduling and demand response integration.

- Establish transparent pricing or cooperative capacity allocation.

- Publish independently verifiable environmental metrics.

## 10.4. Open Standards Ecosystem

- Standardize workload, identity, model, telemetry, and attestation formats.

- Support multiple schedulers and operators.

- Maintain open reference implementations and public conformance tests.

# 11. Questions for Collaborators

Reviewers are invited to challenge the assumptions in this draft and contribute evidence, designs, and counterexamples. The following questions are intended to focus the first review cycle.

- How much distributed compute capacity is realistically available after accounting for ownership, availability, memory, bandwidth, security, and energy efficiency?

- Which measurements can support a fair energy and water comparison between centralized and distributed execution?

- Which combinations of attestation, isolation, encryption, replication, and result verification are practical on heterogeneous nodes?

- How should an enterprise enforce data residency, retention, model licensing, and audit requirements across a trusted federation?

- Which workloads produce a measurable advantage when distributed, and which should remain centralized?

- Which governance and compensation models can support voluntary participation without recreating a dominant intermediary?

- How should local grid, water, noise, land, and community effects be represented in workload placement decisions?

- What is the smallest proof of concept that could test the central claims with reproducible results?

- How does feasibility change across regions with different energy systems, grid reliability, water stress, connectivity, device ownership, costs, climates, laws, and institutions?

# 12. Collaboration and Revision Process

Version 0.1 is intended for structured review rather than endorsement. Comments should identify the relevant section, distinguish factual corrections from design preferences, and include supporting evidence when available. Proposed technical changes should state the expected benefit, operating assumptions, failure modes, and a method of evaluation.

1. Collect comments and unresolved objections without treating disagreement as a request for removal.

1. Revise factual claims when stronger evidence becomes available and preserve the scope and uncertainty of each source.

1. Track material changes by version so reviewers can see which assumptions, requirements, and conclusions changed.

1. Require measurements or reproducible prototypes before making strong claims about cost, efficiency, security, or environmental benefit.

1. Prepare a response to review comments when a later version is released.

# 13. Conclusion

Centralized facilities will remain necessary for some artificial intelligence workloads. They should be used where their technical advantages justify their full environmental and community costs. They should not remain the automatic destination for work that can run locally, regionally, or through a trusted federation.

Public resistance to data center development shows that the current expansion model is encountering physical and community limits. Concerns about electricity, water, air quality, noise, land, utility infrastructure, property rights, and long term local effects are legitimate engineering constraints. A durable infrastructure strategy must include them at the design stage.

The alternative is a governed system for making better use of computing resources that already exist. The guiding rule is to place each workload on the smallest, nearest, most efficient, and most accountable resource capable of performing it. Applied carefully, this approach can reduce unnecessary infrastructure construction, improve data sovereignty, and give organizations a practical option between complete self containment and dependence on hyperscale providers.

# Review and Citation

This document is a working draft. When referring to this version, cite: John D. Midyette, *Distributed Artificial Intelligence Infrastructure*, working draft version 0.1, November 2026. This working draft and the repository documentation are available under the [Creative Commons Attribution 4.0 International License](LICENSE). Citation metadata is provided in [`CITATION.cff`](CITATION.cff). Any future software implementation will be released under a separately identified software license.

# References

[1] Lawrence Berkeley National Laboratory. United States Data Center Energy Usage Report 2025 Update. 2026. [Access source](https://www.energy.gov/documents/united-states-data-center-energy-usage-report-2025-update)

[2] United States Department of Energy. Draft National Transmission Needs Study. 2026. [Access source](https://www.energy.gov/oe/national-transmission-needs-study)

[3] North American Electric Reliability Corporation. Large Loads Action Plan. [Access source](https://www.nerc.com/initiatives/large-loads-action-plan)

[4] Electric Power Research Institute. Partnering for Progress Understanding Community Centered Data Center Development. [Access source](https://community-centered.epri.com/executive-summary.html)

[5] Data Center Watch. Data Center Project Opposition Report. [Access source](https://www.datacenterwatch.org/report)

[6] Data Center Dynamics. Application for 1 3 Billion Dollar Data Center in Chesterton Indiana Withdrawn. June 14 2024. [Access source](https://www.datacenterdynamics.com/en/news/application-for-13bn-data-center-in-chesterton-indiana-withdrawn/)

[7] Data Center Dynamics. Plans for Data Center in Monterey Park Withdrawn. April 2 2026. [Access source](https://www.datacenterdynamics.com/en/news/plans-for-data-center-in-monterey-park-withdrawn/)

[8] Berkeley Lab. The Water Use of Data Center Workloads A Review and Assessment of Key Determinants. 2025. [Access source](https://seta.lbl.gov/publications/water-use-data-center-workloads)

[9] United States Environmental Protection Agency. Clean Air Act Resources for Data Centers. [Access source](https://www.epa.gov/stationary-sources-air-pollution/clean-air-act-resources-data-centers)

[10] United States Department of Energy. Frequently Asked Questions on the National Interest Electric Transmission Corridor Designation Process. [Access source](https://www.energy.gov/oe/frequently-asked-questions-national-interest-electric-transmission-corridor-designation-process)

[11] International Telecommunication Union. Facts and Figures 2026. [Access source](https://www.itu.int/itu-d/reports/statistics/facts-figures-2026/)

[12] Zhang and others. EdgeShard Efficient Large Language Model Inference via Collaborative Edge Computing. IEEE Internet of Things Journal. 2025. [Access source](https://research.polyu.edu.hk/en/publications/edgeshard-efficient-llm-inference-via-collaborative-edge-computin/)
