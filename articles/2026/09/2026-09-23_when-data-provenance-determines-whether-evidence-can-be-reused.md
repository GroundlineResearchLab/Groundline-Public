# When Data Provenance Determines Whether Evidence Can Be Reused

**Date:** 23 September 2026  

**Domain:** Data Provenance and Evidence Reuse  

**Publication Type:** Article

## Context

Data can remain accessible long after the research conditions that gave it meaning have disappeared from view.

A dataset may still be downloadable.

A spreadsheet may still contain every recorded value.

A repository may preserve the file.

A publication may provide a valid citation.

None of those properties, by themselves, establishes that the data can be reliably reused as evidence for a different claim.

The reuse problem begins when another researcher needs to determine what the data actually represent.

Where did the observations originate?

Why were they collected?

Which population or system was inside the original measurement boundary?

What definitions and units were used?

Was the available file raw data or a transformed derivative?

Which version is being reused?

What happened between the original observation and the dataset now available?

Were uncertainty and limitations preserved?

And does the proposed new use remain compatible with the conditions under which the evidence was originally produced?

The FAIR Guiding Principles make an important distinction between accessibility and reusability. Reusability requires rich description, clear usage conditions, detailed provenance, and alignment with relevant community standards.[1]

NIST's Research Data Framework similarly states that metadata are essential to effective use, reuse, and long-term preservation of research data. It treats provenance, version identification, derivative products, aggregation, subsets, and related contextual information as important parts of research data management.[2]

The research question is therefore:

**How does data provenance affect whether existing evidence can be reliably reused in a different research context?**

The central distinctions are:

`Accessible Data ≠ Reusable Evidence`

and:

`Source Citation ≠ Complete Provenance`

A citation can identify a source.

Provenance can preserve the history needed to understand what that source actually represents.

## What the Evidence Shows

Provenance is more than an administrative record attached to a dataset.

The W3C PROV model represents provenance through entities, activities, and agents involved in producing or modifying information. It can express derivation between data objects and identify activities involved in creating one object from another.[3]

W3C also identifies practical uses of provenance including understanding how data were collected so they can be meaningfully used, evaluating trustworthiness, checking processes, and reproducing how an object or result was generated.[3]

The National Academies applies related reasoning to computational research. Its reproducibility guidance emphasizes preserving information about input data, computational steps, methods, code, and conditions of analysis. It also notes the importance of documenting the computational environment and the process through which published results were generated.[4]

Together, these sources show why file availability alone is not enough.

Reuse requires enough preserved context to determine what the data represent and whether a proposed new claim remains compatible with those original evidence conditions.

## 1. Reuse Begins With Evidence Origin

A reusable dataset first needs an identifiable evidentiary origin.

Data may originate from:

- Direct observation.
- Scientific instruments.
- Surveys.
- Administrative systems.
- Financial transactions.
- Satellite imagery.
- Human coding.
- Regulatory records.
- Existing research databases.
- Computational simulations.
- Other derived datasets.
- Multiple upstream sources.

These origins matter because they determine what kind of evidence exists.

Administrative records do not necessarily observe the same population as a population survey.

A modeled estimate is not the same evidence object as a direct measurement.

A dataset compiled from published reports can inherit the limitations of those reports.

A derived dataset may contain no original observations of its own.

Knowing where a file was downloaded is therefore not always sufficient.

For some forms of reuse, researchers need to understand what evidence exists upstream of the immediate file.

## 2. Original Purpose Can Shape Future Reuse

Data are usually created for a reason.

A tax database exists primarily to administer taxation.

A hospital database supports healthcare operations.

A traffic sensor may have been installed to manage traffic flow.

A company database may have been designed for billing.

A research survey may have been designed around a narrowly specified question.

Those systems can later become valuable sources of secondary evidence.

But secondary use does not erase the original design.

GO FAIR guidance on rich metadata recommends documenting the purpose and scope of data collection, relevant limitations, collection conditions, whether data are raw or processed, software versions, and other contextual information useful to future users.[5]

This creates an important distinction:

`Useful for Original Purpose ≠ Automatically Suitable for New Purpose`

The original purpose can influence:

- What was measured.
- What was ignored.
- Which units entered the dataset.
- Which variables were mandatory.
- How categories were defined.
- How frequently observations were recorded.
- Which errors mattered to the original system.

A secondary research question may require evidence that the original system was never designed to produce.

## 3. Population Boundaries Travel With the Data

Suppose a dataset contains every transaction recorded by one digital platform.

It may have excellent internal completeness.

But its population may still be:

`Customers Using Platform A`

rather than:

`All Consumers in the Market`

A later researcher using the dataset for a market-wide claim therefore faces a population problem.

Relevant questions can include:

- Who could enter the original dataset?
- Who could not?
- Did inclusion require registration?
- Were particular groups excluded?
- Did platform coverage change over time?
- Does the new target population match the population represented by the original evidence?

The numerical values do not answer these questions by themselves.

Population boundaries belong to the context of the evidence.

If that context is lost, local evidence can acquire a broader meaning than it originally supported.

## 4. System Boundaries Also Travel With the Data

The same problem applies to non-human systems.

Consider a dataset reporting industrial energy use.

The measurement boundary might include:

`One production line`

or:

`One factory`

or:

`All company facilities`

It might measure:

`Purchased electricity`

or:

`Purchased electricity + onsite generation`

or a still broader energy boundary.

Each dataset may be correct.

They do not necessarily represent the same operational system.

A later user therefore needs enough provenance to understand what was inside and outside the original measurement boundary.

Otherwise values can appear numerically compatible while representing different systems.

## 5. Variable Names Do Not Preserve Their Own Meaning

Consider a field called:

`Capacity`

That label might mean:

- Installed capacity.
- Rated capacity.
- Operational capacity.
- Available capacity.
- Tested capacity.
- Contracted capacity.
- Usable capacity under specified conditions.

The same problem can occur with:

`Employment`

`Output`

`Failure`

`Customer`

`Incident`

`Available`

A later researcher who sees only the variable name may assign a meaning that differs from the one used when the data were produced.

Reusable evidence therefore requires semantic context.

FAIR reusability calls for data and metadata to be richly described and aligned with relevant community standards, while GO FAIR guidance specifically emphasizes explaining variables and preserving contextual attributes required to judge usefulness for another purpose.[1][5]

## 6. Units Need Meaning as Well as Labels

Units may appear easier to preserve.

A dataset can clearly state:

`kg`

`MWh`

`USD`

`hours`

But identical units can describe different quantities.

For example:

`MWh of installed generation capacity`

is not the same measurement as:

`MWh generated`

and neither is the same as:

`MWh available for dispatch`

Similarly, a value reported in USD may depend on whether it represents gross revenue, net revenue, nominal values, real values, tax-inclusive values, or converted currency.

Preserving the unit is necessary.

Preserving what that unit represents is equally important.

## 7. Raw and Processed Data Are Different Evidence Objects

A published dataset may be several transformations removed from the original observations.

For example:

`Sensor Readings`

`→ Filtering`

`→ Calibration`

`→ Missing Value Treatment`

`→ Aggregation`

`→ Published Dataset`

The published data may be entirely legitimate.

But it is no longer identical to the raw evidence.

GO FAIR recommends documenting whether data are raw or processed.[5]

NIST similarly addresses original authoritative copies, derivative products, aggregation, subsets, and version identification within its research data framework.[2]

This distinction matters because a processed dataset may be suitable for one research question and unsuitable for another.

A daily average may be useful for studying long-term conditions.

It may be unsuitable for investigating short-duration extreme events that disappeared during aggregation.

## 8. Transformation History Changes What Can Be Reused

Common transformations include:

- Cleaning.
- Deduplication.
- Filtering.
- Imputation.
- Reclassification.
- Normalization.
- Aggregation.
- Unit conversion.
- De-identification.
- Geocoding.
- Manual correction.
- Algorithmic classification.
- Statistical adjustment.
- Weighting.
- Model-based estimation.

None of these operations is inherently problematic.

Many are necessary.

The problem arises when their existence is no longer visible.

If missing values were imputed, a later researcher may incorrectly interpret all values as direct observations.

If extreme values were removed during cleaning, the resulting dataset may be inappropriate for studying rare events.

If categories were collapsed, later users may no longer be able to recover the distinctions required by a new analysis.

Transformation history therefore affects the evidentiary possibilities that survive into future reuse.

## 9. Derived Data Need Their Lineage

A dataset may move through several stages:

`Dataset A → Dataset B → Dataset C → Dataset D`

Each stage may involve legitimate processing.

But if Dataset D is published without its lineage, a future user may know only the final object.

W3C PROV is specifically designed to represent derivation relationships between entities and the activities through which one entity was produced from another.[3]

This matters because derived evidence can inherit upstream limitations.

These may include:

- Sampling limitations.
- Selection boundaries.
- Missing observations.
- Classification errors.
- Temporal limits.
- Measurement uncertainty.
- Coverage limitations.

Transformation can change the representation of evidence.

It does not automatically eliminate the limitations of the evidence from which it was derived.

## 10. Combining Datasets Creates a New Evidence Object

Secondary research often involves joining existing datasets.

For example:

`Dataset A + Dataset B → Dataset C`

Dataset C is not simply a larger copy of A and B.

The integration itself changes the evidence.

Possible issues include:

- Which identifiers were used for matching.
- Whether unmatched observations were excluded.
- Whether duplicate records were created.
- Whether one-to-many relationships existed.
- Whether the datasets covered the same period.
- Whether definitions aligned.
- Whether missing matches were systematically distributed.

The resulting dataset therefore has its own provenance.

Citing A and B identifies important sources.

It may not fully explain what Dataset C represents after integration.

## 11. Version History Determines Which Evidence Was Used

Datasets change.

Errors are corrected.

Records are added.

Historical values are revised.

Classifications change.

Dynamic databases continue to update.

A dataset title therefore may not uniquely identify the evidence state used in an analysis.

NIST identifies version information as important to traceability and to understanding edits and previous states of research data.[2]

DataCite likewise recommends explicit version information and relationships between major versions, including `IsNewVersionOf`, `IsPreviousVersionOf`, `HasVersion`, and `IsVersionOf` relationships.[6]

A later researcher may therefore need more than:

`Dataset X`

They may need:

`Dataset X + Version + Retrieval Date`

Without this information, two researchers can cite the same dataset name while unknowingly analyzing different evidence.

## 12. Citation and Provenance Solve Different Problems

Citation is essential.

It identifies sources, supports attribution, and helps readers locate referenced material.

But citation and provenance are not equivalent.

A statement such as:

`Source: Dataset X`

may identify where an analyst obtained the data.

It may not reveal:

- Who originally collected the observations.
- Which version was used.
- Whether Dataset X is derived from another source.
- Which transformations occurred.
- Whether categories were changed.
- Whether only a subset was used.
- Whether uncertainty information was removed.

W3C PROV explicitly models relationships among entities, activities, agents, generation, usage, and derivation.[3]

DataCite similarly distinguishes citation relationships from version, part, and other related-resource relationships.[6]

The distinction is therefore:

`Citation → Identifies a Source`

`Provenance → Preserves Relevant Evidence History`

A properly cited dataset can still have insufficient provenance for a particular secondary use.

## 13. Accessibility and Reusability Are Separate Properties

A repository may solve the access problem extremely well.

A file may be:

- Findable.
- Downloadable.
- Machine-readable.
- Citable.
- Openable years later.

That does not automatically establish that another researcher can interpret it correctly.

The FAIR principles explicitly separate Findable, Accessible, Interoperable, and Reusable properties.[1]

For reuse, the principles require rich description, a clear data usage license, detailed provenance, and relevant community standards.[1]

This means that:

`Can Access ≠ Can Reliably Reuse`

Digital availability preserves the object.

Provenance helps preserve its meaning.

## 14. Reproducibility and Reuse Are Related but Different

Provenance also connects reuse with reproducibility.

The National Academies defines computational reproducibility in terms of obtaining consistent computational results using the same input data, computational steps, methods, code, and conditions of analysis.[4]

That is different from asking whether the same data can support a new research claim.

A dataset may allow the original result to be reproduced perfectly while remaining inappropriate for:

- A different population.
- A different period.
- A different outcome.
- A broader geographic claim.
- A different measurement interpretation.

Reproducibility asks whether the original analysis can be regenerated.

Reuse asks whether the evidence remains appropriate for another purpose.

Provenance helps answer both questions, but the evidentiary endpoints differ.

## 15. Reuse Is Claim-Specific

Consider historical temperature measurements from one weather station.

The dataset may support:

**What temperature did this station record on a specified date?**

It may also support:

**What was the distribution of recorded temperatures at this station during that year?**

The same dataset may not establish:

**What was the average temperature across the entire country?**

And historical data cannot directly establish:

**What is the country's temperature today?**

The dataset did not change.

The claim did.

This distinction can be expressed as:

`Reusable for Claim A ≠ Reusable for Claim B`

Provenance helps preserve the boundaries needed to see that difference.

## 16. Reuse Across Contexts Inherits the Comparability Problem

When evidence is reused, it effectively moves from an original research context into a new one.

The original data may have been produced within one:

- Population.
- Geography.
- Institution.
- Regulatory system.
- Time period.
- Measurement boundary.
- Sampling system.
- Operating environment.

The new analysis may concern another.

If those differences materially affect the proposition being tested, direct reuse may require qualification, adjustment, or different evidence.

This is the same underlying problem encountered in cross-context comparison.

Valid evidence in its original context is not automatically valid for every new context.

## 17. Context Can Be Lost While the Data Survive

Consider a surviving table:

| Facility | Value |
| --- | ---: |
| A | 100 |
| B | 85 |
| C | 120 |

The file may be technically perfect.

But without contextual information, a later user may not know:

- What the values measure.
- Which units apply.
- When they were recorded.
- Whether they are estimates.
- Whether values were normalized.
- Whether some facilities were excluded.
- Whether 100 means capacity, production, consumption, or an index.

The bytes survived.

The evidentiary meaning did not.

NIST specifically warns that weak metadata make reuse and preservation more difficult and time-intensive.[2]

This is why long-term data preservation is not only a storage problem.

It is also a meaning-preservation problem.

## 18. Uncertainty Can Be Lost During Reuse

A central estimate can survive while its qualifications disappear.

Suppose the original evidence contains:

`Estimate = 50`

`Confidence Interval = 30 to 70`

A downstream dataset preserves only:

`50`

The central value remains.

The uncertainty does not.

Other information can disappear in the same way:

- Quality flags.
- Detection limits.
- Provisional status.
- Imputation indicators.
- Sampling errors.
- Calibration uncertainty.
- Model assumptions.
- Known data gaps.

Removing these attributes can make downstream evidence appear more certain than the original evidence actually was.

Preserving evidentiary context therefore includes preserving material uncertainty.

## 19. Subsets and Aggregates Change Reuse Possibilities

Researchers frequently reuse only part of a dataset.

For example:

`National Dataset → Region A`

or:

`2010 to 2025 Dataset → 2020 to 2025`

or:

`All Firms → Large Firms Only`

The subset may be appropriate.

But it is now a derived evidence object.

Its interpretation depends partly on the source dataset, version, selection rule, and any observations removed.

Aggregation produces a related problem.

Individual records may be converted into monthly totals.

The resulting dataset may remain useful for studying monthly volume.

It may no longer support:

- Event timing.
- Distribution analysis.
- Individual behavior.
- Intraday variation.
- Duplicate detection.

The data are not necessarily invalid.

The transformation changed what they can establish.

## 20. Secondary Reuse Creates New Provenance

A secondary analyst often changes the data they receive.

They may:

- Convert units.
- Merge categories.
- Recode variables.
- Exclude observations.
- Add external sources.
- Construct new indicators.
- Calculate ratios.
- Apply new models.

At that point, the secondary analysis becomes another stage in the data lineage.

The original provenance does not end.

It is extended.

The resulting evidence should remain traceable both to its upstream sources and to the new transformations introduced during reuse.

## 21. Provenance Supports Error Tracing

Suppose Dataset A contains a classification error.

Dataset B derives from A.

Dataset C combines B with another source.

Several publications reuse C.

If lineage is preserved:

`A → B → C → Publications`

researchers can identify which downstream products may have inherited the problem.

Without provenance, the same error can appear independently in many outputs while its common origin remains hidden.

Versioning matters here as well.

If the repository later publishes a corrected version, researchers need to know whether an analysis used the earlier or corrected dataset.

This makes provenance useful not only for reuse.

It also supports correction.

## 22. Permission and Evidentiary Suitability Are Different Questions

Reuse also has legal and governance boundaries.

A dataset may be methodologically suitable for a proposed analysis while its licence or access conditions do not permit that use.

Another dataset may be openly licensed while being evidentially unsuitable for the claim.

FAIR includes clear usage licensing as part of reusability.[1]

NIST also addresses licences, usage agreements, intellectual-property considerations, sensitive data, and jurisdictional issues within research data management.[2]

The distinction is:

`Permitted to Reuse ≠ Evidentially Appropriate to Reuse`

and:

`Evidentially Appropriate ≠ Automatically Permitted`

Both may matter in responsible evidence reuse.

## 23. Strong Provenance Can Show That Data Should Not Be Reused

Provenance does not exist to maximize reuse regardless of context.

Detailed provenance can reveal that a dataset is inappropriate for a proposed claim.

For example, it may show that:

- The target population excludes the group now being studied.
- Modeled values are being treated as direct observations.
- A variable changed definition.
- The data were aggregated beyond the resolution required.
- Important observations were removed during processing.
- The new claim concerns a period outside the dataset.
- A transformation changed the meaning of the relevant variable.

In these situations, discovering that reuse is inappropriate is not a failure.

It is evidence that provenance is doing its job.

## 24. Provenance Requirements Depend on the New Use

Not every reuse requires the same documentation.

A simple historical reference may require a relatively limited evidence record.

A detailed statistical reanalysis may require substantially more information about:

- Population.
- Sampling.
- Definitions.
- Weights.
- Processing.
- Version.

Computational reproduction may additionally require:

- Code.
- Parameters.
- Software.
- Computational environment.
- Workflow.

Cross-context reuse may require strong information about the original population, measurement boundaries, definitions, transformations, and limitations.

The National Academies emphasizes this greater level of detail where computational results depend on data, code, and workflows.[4]

There is therefore no single provenance record that guarantees suitability for every possible future research question.

## 25. Reuse Should Not Silently Expand the Evidence Boundary

Evidence can acquire a broader meaning as it moves downstream.

The original research may state:

`Observed Among Survey Respondents`

A secondary publication may describe the same result as:

`Observed Among Workers`

A later summary may transform it again into:

`Observed Across the Economy`

The underlying numerical value may be unchanged.

The claim boundary has expanded.

Provenance helps reconnect the downstream statement to the population, place, period, and measurement conditions that produced the evidence.

Reuse may transform analysis.

It should not silently transform what the original evidence represented.

## Why It Matters

Data reuse is becoming easier.

Repositories preserve more datasets.

Persistent identifiers improve discovery.

Research infrastructures connect publications and data.

Software can merge large datasets rapidly.

Automated systems can retrieve and analyze evidence that the analyst did not personally collect.

These developments increase the value of existing data.

They also increase the distance between the person reusing evidence and the conditions under which that evidence was created.

That distance makes provenance more important.

Without sufficient provenance, researchers may know the number but not the measurement.

They may know the file but not the population.

They may know the citation but not the transformation.

They may know the dataset name but not the version.

They may know an output without knowing which assumptions or processing decisions produced it.

The central question is therefore not simply:

**Can this dataset be obtained?**

It is:

**Is enough of its evidentiary history preserved to determine whether it supports the new claim?**

That is the point at which provenance becomes a condition of reliable evidence reuse.

## Limits and Uncertainty

This article does not propose that all datasets require identical provenance documentation.

A historical administrative record, laboratory dataset, survey, sensor stream, derived statistical database, and computational model output can require different levels and forms of documentation.

W3C PROV provides a general model for representing provenance relationships. It does not establish a universal evidence-quality threshold for reuse.[3]

The FAIR Guiding Principles provide high-level goals for findability, accessibility, interoperability, and reusability. They do not prescribe one universal implementation system.[1]

NIST's Research Data Framework is likewise intended as a flexible and non-prescriptive research data management resource.[2]

The National Academies guidance cited here focuses strongly on computational reproducibility. Detailed information about software environments, code, and computational workflows will not be equally relevant to every dataset.[4]

DataCite provides mechanisms for identifying versions and relationships among research objects. Persistent identifiers and version links do not themselves establish that a dataset is methodologically appropriate for a particular secondary claim.[6]

The public sources reviewed do not establish that:

- Data without perfect provenance are always unusable.
- Every reuse requires access to raw data.
- Every derived dataset is weaker than its source.
- Every transformation reduces evidence quality.
- A persistent identifier guarantees methodological validity.
- Reproducibility automatically establishes suitability for secondary use.
- Openly accessible data can be reused for any purpose.
- Detailed provenance guarantees that a new claim is valid.

The broader principle is narrower:

**Data should not lose the history required to understand what they represent.**

A dataset can remain technically available after its evidentiary context has been lost.

A citation can remain correct while the relevant production history remains unclear.

A dataset can be computationally reproducible while being incompatible with a new research population or claim.

And a richly documented dataset can reveal that it should not be reused for a particular purpose.

That is not a failure of provenance.

It is precisely what provenance can make visible.

`Accessible Data ≠ Reusable Evidence`

and:

`Source Citation ≠ Complete Provenance`

Reliable evidence reuse requires enough preserved history to understand the original evidence, identify material transformations and versions, preserve relevant limitations, and determine whether the original evidence boundaries remain compatible with the new claim.

## Sources

**[1] Wilkinson MD, Dumontier M, Aalbersberg IJ, et al.** "The FAIR Guiding Principles for Scientific Data Management and Stewardship." *Scientific Data*. Published 15 March 2016. Foundational FAIR publication defining Findable, Accessible, Interoperable, and Reusable as distinct objectives. Reusability includes rich metadata, clear data usage licensing, detailed provenance, and domain-relevant community standards.

**DOI:** 10.1038/sdata.2016.18

**URL:** https://doi.org/10.1038/sdata.2016.18

**Accessed:** 23 September 2026.

**[2] National Institute of Standards and Technology.** *NIST Research Data Framework (RDaF), Version 2.0.* NIST Special Publication 1500-18r2. February 2024. Research data management framework addressing metadata and provenance, data use and reuse, original authoritative copies, derivative products, aggregation, subsets, version identification, licensing, and other research-data lifecycle considerations.

**DOI:** 10.6028/NIST.SP.1500-18r2

**URL:** https://doi.org/10.6028/NIST.SP.1500-18r2

**Accessed:** 23 September 2026.

**[3] World Wide Web Consortium Provenance Working Group.** *PROV Model Primer.* W3C Working Group Note. 30 April 2013. Introductory documentation for the W3C PROV family explaining entities, activities, agents, generation, use, and derivation and describing applications including meaningful data use, trust assessment, process verification, and reproduction.

**URL:** https://www.w3.org/TR/prov-primer/

**Accessed:** 23 September 2026.

**[4] National Academies of Sciences, Engineering, and Medicine.** *Reproducibility and Replicability in Science.* Washington, DC: The National Academies Press. 2019. Consensus study report defining computational reproducibility and emphasizing information about data, computational steps, methods, code, conditions of analysis, computational environments, and provenance needed to reproduce scientific results.

**DOI:** 10.17226/25303

**URL:** https://doi.org/10.17226/25303

**Accessed:** 23 September 2026.

**[5] GO FAIR.** "R1: (Meta)data are richly described with a plurality of accurate and relevant attributes." FAIR implementation guidance. Recommends preserving contextual metadata including data purpose and scope, limitations, collection conditions, processing state, software versions, variable meanings, and dataset versions so future users can evaluate usefulness in another context.

**URL:** https://www.go-fair.org/fair-principles/r1-metadata-richly-described-plurality-accurate-relevant-attributes/

**Accessed:** 23 September 2026.

**[6] DataCite.** "Versioning." Research metadata guidance describing use of version metadata, version-specific identifiers, and relationships including `IsNewVersionOf`, `IsPreviousVersionOf`, `HasVersion`, and `IsVersionOf` to distinguish and connect different states of research objects.

**URL:** https://support.datacite.org/docs/versioning

**Accessed:** 23 September 2026.

---

**Groundline Research Lab**  

**Data • Evidence • Provenance • Research Systems**  

Under the DGCP™ framework
