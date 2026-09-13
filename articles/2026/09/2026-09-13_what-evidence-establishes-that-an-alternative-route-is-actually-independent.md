# What Evidence Establishes That an Alternative Route Is Actually Independent?

**Date:** 13 September 2026

**Domain:** Infrastructure Evidence and Resilience

**Publication Type:** Article

## Context

Infrastructure maps often make redundancy appear simple.

A primary route connects two points. A second route also connects them. The second line may therefore be described as an alternative, backup, bypass, redundant path, or independent route.

But the existence of two physical paths does not establish that either can substitute for the other during a disruption.

A second route may depend on the same power supply, terminal, pumping station, switching facility, control system, communications network, port, bridge, upstream source, downstream receiving facility, or operating organization as the primary route.

It may also pass through a different corridor while remaining exposed to the same flood, wildfire, conflict zone, cyber system, regulatory restriction, or other failure condition.

The evidence question is therefore not simply whether another route exists.

It is:

**What evidence is sufficient to establish that infrastructure functions as an independent backup rather than merely an alternative route?**

A useful evidence chain is:

`Physical Route → Operating Capacity → Geographic Separation → Threat Exposure → Dependency Separation → Switching Capability → Usable Capacity → Disruption Performance`

The distinction at the center of that chain is:

`Alternative Route ≠ Independent Backup`

## What the Evidence Shows

Existing resilience and reliability guidance already treats redundancy as more than duplication.

The U.S. Cybersecurity and Infrastructure Security Agency describes infrastructure dependencies as relationships of reliance within and among infrastructure assets and systems. It identifies physical, geographic, cyber, and logical forms of dependency and notes that disruption in one infrastructure system can produce cascading effects across others.[1]

CISA's guidance on backup systems and redundant providers goes further. When evaluating backup services, it recommends asking whether the backup depends on other systems, whether critical interconnections exist, and whether a redundant provider is also relied upon by multiple other systems.[2]

The National Institute of Standards and Technology applies a similar principle in contingency planning for federal information systems. Its guidance states that an alternate facility must be capable of supporting required system operations. It also recommends locating fixed alternate sites where they are unlikely to be negatively affected by the same hazard as the primary site.[3]

Transmission reliability standards provide another form of the same logic. NERC's TPL-001-5.1 requires planning studies and contingency analyses to assess Bulk Electric System performance under specified system conditions and planning events.[4]

Nuclear safety literature provides an especially explicit illustration of why redundancy does not guarantee independence. U.S. Nuclear Regulatory Commission material addresses common-cause failure potential where a condition affecting one component could also affect other redundant components within the same common-cause component group.[5]

These sources come from different infrastructure domains and should not be treated as one universal engineering standard.

But they support a common evidence principle:

**Redundancy has to be evaluated against failure conditions, not inferred from the existence of a second asset.**

## 1. Physical Route Existence

The first layer is the easiest to establish.

Does another route physically exist?

Evidence might include:

* Official infrastructure maps.
* Operator maps.
* Regulatory filings.
* Engineering plans.
* Geographic information system data.
* Satellite imagery.
* Construction records.
* Commissioning documentation.

This evidence can establish that two corridors, lines, pipelines, cables, roads, transmission circuits, or other physical paths exist.

It cannot by itself establish that both are operational.

A mapped line may be incomplete, inactive, under maintenance, constrained, reserved for another purpose, or dependent on infrastructure shared with the primary route.

Physical existence is therefore evidence of topology.

It is not yet evidence of backup capability.

## 2. Operational Availability

The next question is whether the alternative can actually operate.

An asset may physically exist while being unavailable because of:

* Maintenance.
* Damage.
* Seasonal restrictions.
* Regulatory limitations.
* Insufficient staffing.
* Missing equipment.
* Lack of upstream supply.
* Lack of downstream receiving capacity.
* Contractual allocation.
* Operating configuration.
* Safety restrictions.

Evidence of operational availability therefore requires more than a map.

Relevant evidence may include operator status reports, maintenance records, regulatory disclosures, operating notices, system telemetry, flow data, shipping records, dispatch information, or other records showing that the infrastructure can actually perform its intended function.

This creates the first major distinction:

`Exists ≠ Available`

## 3. Rated Capacity

If the alternative is operational, the next question is how much capacity it was designed or rated to provide.

Examples include:

* Pipeline throughput.
* Transmission capacity.
* Railway train capacity.
* Road or bridge traffic capacity.
* Port handling capacity.
* Data transmission bandwidth.
* Water transfer capacity.
* Processing capacity.

Rated capacity can be important evidence.

But it is normally a property of the asset or design under specified conditions.

It should not automatically be interpreted as the amount of capacity available during a particular disruption.

A route rated for a given throughput may be constrained by another component in the chain.

For example, a pipeline may have sufficient line capacity while the available pumping, loading, storage, or terminal capacity is lower.

A transmission line may have a nominal rating while system conditions prevent that full rating from being used after another element fails.

A transport corridor may physically support a certain volume while terminals or connecting networks cannot receive that volume.

The evidence distinction is therefore:

`Rated Capacity ≠ Available Capacity`

## 4. Actually Usable Capacity

The relevant resilience question is usually not how much capacity the route theoretically possesses.

It is how much capacity remains usable under the disruption being examined.

Usable capacity may be limited by the weakest necessary part of the operating chain.

Conceptually:

`Usable Backup Capacity = Capacity Remaining Across the Required End-to-End System`

This is not a universal engineering formula.

It is an evidence framework.

If an alternative route requires several systems to function together, evidence about the route alone is insufficient.

Researchers may need to examine:

* Entry capacity.
* Exit capacity.
* Transfer points.
* Terminals.
* Storage.
* Pumps or compressors.
* Substations.
* Switching equipment.
* Communications.
* Control systems.
* Upstream supply.
* Downstream demand or receiving infrastructure.
* Operating personnel.
* Regulatory or contractual restrictions.

A route with high nominal capacity can therefore provide much less effective backup capacity if another required component becomes the binding constraint.

## 5. Geographic Separation

Two routes can be physically different without being geographically independent.

The relevant question is whether the separation is sufficient for the failure condition being considered.

A few kilometers of separation may protect against one local equipment failure.

It may provide little protection against:

* Regional flooding.
* Earthquake.
* Wildfire.
* Severe weather.
* Military conflict.
* Large-scale power failure.
* Port closure.
* Regional evacuation.
* A disruption affecting an entire narrow corridor.

NIST's contingency planning guidance illustrates this distinction by recommending that fixed alternate sites be located where they are unlikely to be negatively affected by the same hazard as the primary site.[3]

The relevant evidence is therefore not simply distance.

It is:

`Geographic Separation Relative to the Threat`

A route can be geographically separate for one hazard and remain inside the same failure domain for another.

## 6. Shared Infrastructure Dependencies

Physical separation becomes less meaningful when two routes rely on the same supporting asset.

Consider two otherwise separate routes that share one:

* Terminal.
* Port.
* Bridge.
* Pumping station.
* Electrical substation.
* Control center.
* Communications link.
* Data center.
* Fuel supply.
* Water source.
* Border crossing.
* Storage facility.

Failure of the shared component may remove both routes simultaneously.

This is why dependency evidence matters.

CISA identifies dependencies as physical, geographic, cyber, or logical and emphasizes that infrastructure systems can depend on one another in ways that produce cascading disruption.[1]

A claim of independent backup therefore requires evidence about the infrastructure surrounding the route, not only the route itself.

A second path sharing critical single points of failure may provide route diversity without providing full system redundancy.

## 7. Common Threat Exposure

Infrastructure can also be separate in physical design while remaining exposed to the same threat or failure mechanism.

Examples include two routes that:

* Use separate equipment but lie inside the same floodplain.
* Use separate power feeds but depend on the same regional grid.
* Follow different corridors but cross the same conflict area.
* Use different communication links but depend on a common software or control layer.
* Use separate facilities operated through the same control center.
* Depend on different components that share a material design vulnerability.

This is one form of the broader common-cause problem.

NRC material demonstrates why redundant components cannot automatically be assumed to fail independently. In the regulatory context examined by NUREG-2225, a performance deficiency affecting one component can increase concern about common-cause failure affecting other redundant components within the same common-cause component group.[5]

For evidence analysis, this means that independence cannot be established by counting assets.

The relevant failure mechanism must also be examined.

## 8. Control and Operating Dependencies

Infrastructure does not operate only through physical components.

It also depends on control and decision systems.

Two physical routes may share:

* Supervisory control systems.
* Communications networks.
* Authentication systems.
* Dispatch platforms.
* Operations centers.
* Software.
* Data services.
* Personnel.
* Operating procedures.
* Decision authority.

A disruption to one of these layers may make both routes unavailable even when neither physical route is damaged.

This matters especially where infrastructure is digitally monitored, coordinated, or controlled.

Evidence of physical diversity therefore does not establish control independence.

The evidence chain may need to include:

`Physical Separation → Control Separation → Communications Separation → Operating Authority`

Whether each layer matters depends on the infrastructure being examined.

## 9. Switching and Rerouting Capability

An alternative can exist and remain functional without being immediately usable as a backup.

There must also be a mechanism for transferring activity from the primary route.

Questions include:

* Can flow be redirected?
* Can traffic be rerouted?
* Can switching occur remotely?
* Is manual intervention required?
* Does transfer require shutdown?
* How long does reconfiguration take?
* Does the receiving route have spare capacity?
* Are contractual or regulatory approvals required?
* Are compatible connections already installed?
* Has the procedure been tested?

A route that requires several days of physical modification cannot provide the same type of redundancy as a route that can accept traffic immediately.

This creates another distinction:

`Available Alternative ≠ Transferable Backup`

Time is part of usable capacity.

## 10. Performance Under Disruption

The strongest evidence of backup capability is not the existence of a design claim.

It is evidence about performance under the conditions for which the backup is supposed to exist.

NERC's transmission planning requirements illustrate this logic by requiring studies of system performance following specified planning events and contingencies rather than treating the presence of additional network elements as sufficient evidence of reliable performance.[4]

Evidence of disruption performance may come from:

* Contingency simulations.
* Stress tests.
* Emergency exercises.
* Historical disruptions.
* Actual rerouting events.
* Operator records.
* Flow or throughput data.
* Restoration reports.
* Post-incident reviews.

Historical operation can be particularly informative because it shows whether nominal redundancy translated into actual service under a specific disruption.

But historical evidence also requires caution.

Successful performance during one disruption does not establish independence from every other threat.

The relevant claim must remain tied to the tested condition.

## An Evidence Ladder for Independent Backup

Claims about infrastructure redundancy can therefore be separated into different evidence levels.

| Evidence Level            | What the Evidence Establishes                                                                         |
| ------------------------- | ----------------------------------------------------------------------------------------------------- |
| Mapped alternative        | A second physical path is represented                                                                 |
| Verified physical asset   | The alternative infrastructure exists                                                                 |
| Operational route         | The asset is capable of operating                                                                     |
| Rated capacity            | A stated design or operating capacity exists                                                          |
| Available capacity        | Capacity is available under specified conditions                                                      |
| Geographic separation     | The routes occupy sufficiently distinct physical locations for a defined threat                       |
| Dependency separation     | Critical supporting infrastructure is not materially shared for the failure condition being examined  |
| Threat separation         | The routes are not exposed to the same relevant failure mechanism                                     |
| Transfer capability       | Activity can actually be moved to the alternative                                                     |
| Usable backup capacity    | The required end-to-end system can carry replacement activity                                         |
| Contingency performance   | Models, tests, or events show continued operation after a specified disruption                        |
| Demonstrated independence | Evidence shows the alternative remains usable under the failure condition affecting the primary route |

These levels should not be collapsed.

A map can establish an alternative path.

An engineering specification can establish nominal capacity.

Neither alone establishes independent redundancy.

## Independence Is Failure-Specific

One reason redundancy claims are difficult to evaluate is that independence is not always an absolute property.

Consider two routes that have separate physical corridors but use the same control center.

They may be independent from a localized physical obstruction.

They may not be independent from failure of the control center.

Two routes using different control systems might survive that event but remain exposed to the same earthquake.

Two geographically distant facilities might survive the earthquake but rely on the same upstream supplier.

The correct research question is therefore:

**Independent from what failure?**

Without that condition, the term "independent" can become too broad to verify.

A more precise claim would identify both the backup function and the failure domain.

For example:

`Route B provides independent backup against failure of Segment X`

is more testable than:

`Route B is an independent backup route.`

The first claim identifies a condition against which evidence can be evaluated.

The second risks implying universal independence.

## What Evidence Would Support a Stronger Independence Claim?

No single document necessarily proves that an alternative is independent.

The conclusion may require combining different types of evidence.

A strong public evidence package could include:

1. An authoritative map establishing separate physical routes.
2. Operator documentation establishing operational status.
3. Technical documentation establishing capacity.
4. Evidence showing the capacity available under the relevant contingency.
5. Geographic evidence showing separation from the identified threat.
6. Dependency mapping identifying shared and independent supporting infrastructure.
7. Documentation of control and communications architecture where material.
8. Evidence that traffic, energy, data, water, or another service can actually be transferred.
9. Simulation, test, or historical evidence showing performance during disruption.
10. Documentation of any remaining shared failure conditions.

The conclusion should then match the evidence.

If only the first item is established, the appropriate description may be:

**alternative physical route**

not:

**independent backup**

## Why It Matters

The distinction matters because infrastructure terminology can create an impression of resilience before resilience has been demonstrated.

Terms such as:

`backup`

`redundant`

`alternative`

`bypass`

`secondary`

`diverse`

`independent`

may describe different properties.

When these words are treated as interchangeable, a physical infrastructure fact can become an unsupported resilience conclusion.

That can distort assessments of:

* Supply security.
* Transport resilience.
* Energy continuity.
* Network reliability.
* Emergency planning.
* Investment requirements.
* Critical infrastructure exposure.

The evidence standard should therefore remain simple:

**Do not infer independent redundancy from route existence alone.**

Establish the route.

Establish its capacity.

Establish its dependencies.

Establish its threat exposure.

Establish that transfer is possible.

Then examine whether it remains usable under the failure condition that disables the primary route.

Only then can the strength of the redundancy claim be evaluated.

## Limits and Uncertainty

There is no single universal definition of "independent backup" that applies unchanged across pipelines, electricity networks, telecommunications, transportation systems, data infrastructure, water systems, and other infrastructure domains.

Different sectors use different engineering standards, operating criteria, contingency assumptions, and definitions of acceptable performance.

The sources reviewed for this article therefore support an evidence framework rather than a universal technical certification standard.

NIST contingency planning guidance applies specifically to federal information systems.[3]

NERC TPL-001-5.1 applies to planning for the North American Bulk Electric System.[4]

NRC common-cause failure material concerns nuclear safety risk assessment and should not be transferred directly into unrelated infrastructure regulation.[5]

CISA's Infrastructure Dependency Primer provides broader resilience concepts but does not establish asset-specific engineering performance.[1][2]

These sources nevertheless support a consistent analytical distinction:

Physical duplication, geographic separation, nominal capacity, and official designation each provide useful evidence.

None establishes operational independence on its own.

The decisive question remains whether the alternative can continue performing the required function under the conditions that impair the primary route.

That is the difference between having another route and having independent backup.

## Sources

**[1] Cybersecurity and Infrastructure Security Agency.** *Infrastructure Dependency Primer: Learn.* U.S. Department of Homeland Security. Primary government resilience guidance describing physical, geographic, cyber, and logical infrastructure dependencies and cascading effects.

**URL:** https://www.cisa.gov/topics/critical-infrastructure-security-and-resilience/resilience-services/infrastructure-dependency-primer/learn

**Accessed:** 13 September 2026.

**[2] Cybersecurity and Infrastructure Security Agency.** *Infrastructure Dependency Primer: Implement.* U.S. Department of Homeland Security. Primary government resilience guidance addressing backup systems, redundant providers, critical interconnections, and dependencies affecting alternative services.

**URL:** https://www.cisa.gov/topics/critical-infrastructure-security-and-resilience/resilience-services/infrastructure-dependency-primer/implement

**Accessed:** 13 September 2026.

**[3] National Institute of Standards and Technology.** *Contingency Planning Guide for Federal Information Systems.* NIST Special Publication 800-34 Revision 1. Published May 2010; updated 11 November 2010. Primary technical guidance addressing alternate sites, operational readiness, supporting infrastructure, and geographic exposure to common hazards.

**Identifier:** NIST SP 800-34 Rev. 1
**DOI:** 10.6028/NIST.SP.800-34r1

**URL:** https://csrc.nist.gov/pubs/sp/800/34/r1/upd1/final

**Accessed:** 13 September 2026.

**[4] North American Electric Reliability Corporation.** *TPL-001-5.1: Transmission System Planning Performance Requirements.* Primary reliability standard requiring transmission planning studies and contingency analysis across specified planning events and system conditions.

**Identifier:** TPL-001-5.1

**URL:** https://www.nerc.com/pa/Stand/Reliability%20Standards/TPL-001-5.1.pdf

**Accessed:** 13 September 2026.

**[5] U.S. Nuclear Regulatory Commission.** *Basis for the Treatment of Potential Common-Cause Failure in the Significance Determination Process.* NUREG-2225. September 2018. Primary government technical source addressing common-cause failure potential among redundant components in risk assessment.

**Identifier:** NUREG-2225

**URL:** https://www.nrc.gov/reading-rm/doc-collections/nuregs/staff/sr2225/index

**Accessed:** 13 September 2026.

---

**Groundline Research Lab**

**Data • Evidence • Provenance • Research Systems**

Under the DGCP™ framework
