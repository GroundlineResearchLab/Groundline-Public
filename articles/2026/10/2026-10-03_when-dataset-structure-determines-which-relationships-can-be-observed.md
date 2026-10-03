# When Dataset Structure Determines Which Relationships Can Be Observed

**Date:** 3 October 2026  
**Domain:** Dataset Structure and Analytical Connectivity  
**Publication Type:** Article

## Context

A dataset does not merely contain information.

It also determines how that information can be connected.

One table may contain employee characteristics.

Another may contain company characteristics.

Both datasets may be accurate.

Both may contain variables relevant to the same research question.

Yet researchers may still be unable to determine which employee worked for which company.

The missing element is not necessarily information about workers or companies.

It is the relationship between them.

The same problem appears across many evidence systems.

One dataset may contain:

`Income`

and another:

`Education`

without allowing the same individuals to be identified across both.

A production database may contain:

`Factory Output`

while another contains:

`Electricity Consumption`

without identifying which electricity record belongs to which factory.

A business dataset may contain company identifiers and years while administrative identifiers change after restructuring, making apparently continuous entities difficult to track.

A geographic dataset may describe observations by municipality while another uses postal zones.

Both may describe the same general territory.

Their records are not automatically connectable.

The central distinctions are:

`Available Data ≠ Observable Relationship`

and:

`Relevant Variables ≠ Linkable Records`

The research question is:

**How does dataset structure determine which relationships researchers are capable of observing?**

## What the Evidence Shows

Formal data standards treat structure as part of the meaning and usability of data.

The W3C Model for Tabular Data describes a row as a set of cells containing information about a particular thing. It allows one or more cells to function as a primary key whose combined values uniquely identify the row.[1]

The W3C metadata model also supports foreign keys, which allow values in one table to reference a unique row in another table.[2]

Statistical data standards express the same principle differently.

The W3C RDF Data Cube model defines observations through dimensions, measures, and attributes. Dimensions identify what an observation applies to, such as time or geographic area. Measures represent the phenomenon being observed, while attributes provide qualifying information such as units or observation status.[3]

SDMX likewise defines statistical datasets through dimensions, measures, attributes, and keys. The combination of dimensions identifies an observation, with time represented as a formal dimension where relevant.[4]

These standards support a broader evidence principle:

**Information becomes analytically connectable only when the dataset preserves the structural relationships required by the question.**

## 1. The Unit of Observation Determines What One Record Means

Before datasets can be connected, researchers need to know what one record represents.

A record might represent:

- A person.
- A household.
- A job.
- A transaction.
- A company.
- An establishment.
- A geographic area.
- A hospital visit.
- A sensor reading.
- A product.
- A person-year.
- A company-quarter.

These units are not interchangeable.

Suppose one dataset contains one row per person.

Another contains one row per job.

One person may hold more than one job.

Therefore:

`Person ≠ Job`

A simple one-row-to-one-row merge would misrepresent the underlying relationship.

Dataset structure begins with a basic question:

**What does one record represent?**

Without that answer, apparently compatible variables can be connected incorrectly.

## 2. The Same Organization Can Exist at Several Structural Levels

Business data provide a clear example.

An economic organization may appear as:

`Firm`

`Employer`

`Establishment`

`Worksite`

These terms can refer to different evidence units.

U.S. Census Bureau LEHD documentation distinguishes state employer identifiers, establishments, and national firms.[5]

For single-unit firms, some of these structures may coincide.

For multi-unit firms, one firm may contain several establishments and may also be associated with more than one state employer identifier.[5]

This means:

`Employment at Establishment`

is not structurally identical to:

`Employment at Firm`

even though both concern the same wider organization.

The analytical level of the record therefore matters.

## 3. Identifiers Can Make Relationships Explicit

Consider:

| Worker ID | Age |
| --- | ---: |
| P101 | 28 |
| P102 | 44 |

and:

| Worker ID | Earnings |
| --- | ---: |
| P101 | 45,000 |
| P102 | 70,000 |

The relationship can be constructed because:

`P101 in Dataset A = P101 in Dataset B`

The identifier provides a structural bridge.

Without that bridge, the datasets may still contain:

`Age`

and:

`Earnings`

but may not establish which age observation corresponds to which earnings observation.

Identifiers therefore do more than label records.

When their meaning is appropriate to the analysis, they can make relationships between records explicit.

## 4. Primary Keys Define Record Identity

A primary key answers:

**Which record is this?**

It can consist of one field:

`PersonID`

or several fields:

`FirmID + Year`

`StationID + Timestamp`

`Country + Indicator + Year`

The W3C tabular-data model allows the primary key of a row to consist of multiple cells whose combined values uniquely identify that row.[1]

SDMX uses a comparable multidimensional principle for statistical observations: dimension values combine into a key identifying an observation.[4]

This matters because identity may depend on context.

`Firm 123`

identifies an entity.

`Firm 123 + 2026`

identifies an observation concerning that entity at a particular time.

Those are related but different evidence objects.

## 5. Foreign Keys Preserve Relationships Between Evidence Objects

Not every analytical system needs to place every variable in one table.

Consider:

### People

`PersonID | Age | Education`

### Jobs

`JobID | PersonID | EmployerID | Earnings`

### Employers

`EmployerID | Industry | Location`

The structure preserves:

`Person → Job`

and:

`Job → Employer`

A researcher can then examine relationships such as worker education, job earnings, and employer industry.

W3C tabular metadata formally supports this through foreign keys that reference unique rows in another table.[2]

The relationship is represented in the structure.

It does not need to be inferred from row order, name similarity, or proximity in a file.

## 6. Relevant Variables Can Exist Without a Relationship Path

Suppose:

`Dataset A: Income`

and:

`Dataset B: Education`

Both variables are relevant to a question about the relationship between education and income.

But if the datasets contain no defensible common person identity, they do not establish:

`Education of Person X ↔ Income of Person X`

Researchers might still compare:

- Distributions.
- Population averages.
- Regional patterns.
- Group differences.

They cannot automatically estimate the individual-level relationship between those variables.

The evidence state becomes:

`Relevant Information Available`

but:

`Record Relationship Missing`

That is a structural limitation.

It is not simply another missing variable.

## 7. Inferred Linkage Creates an Additional Evidence Process

A common identifier is not always available.

Researchers may instead attempt linkage using combinations of fields such as:

- Name.
- Address.
- Date of birth.
- Organization name.
- Location.
- Other identifying characteristics.

The U.S. Census Bureau uses probabilistic linkage to connect incoming records to a reference file using information including name, address, date of birth, and Social Security Number.[6]

When a linkage can be established, a Protected Identification Key can be appended to support connections with other Census-held data.[6]

This demonstrates that structural connectivity can sometimes be created after data collection.

But the relationship now depends on a linkage process.

The connection itself becomes part of the evidence provenance.

## 8. Linkage Creates False Positive and False Negative Risks

The Office for National Statistics identifies two important linkage errors.[7]

A false positive occurs when records relating to different entities are linked.

A false negative occurs when records relating to the same entity fail to link.

Therefore:

`Records Joined ≠ Relationship Automatically Correct`

ONS also states that match rate alone does not measure linkage quality and recommends evaluation using precision and recall.[7]

A derived dataset created through linkage can therefore contain uncertainty not only about measured values but also about whether particular records belong together.

Relationship uncertainty becomes part of the analytical evidence.

## 9. Additional Linkages Can Add Additional Dependencies

Suppose an analytical dataset is constructed through:

`Dataset A → Dataset B → Dataset C → Dataset D`

Each additional linkage creates another dependency.

Even when every source dataset is individually high quality, the final analytical table can inherit uncertainty from the operations used to connect them.

The final table may look complete.

Its provenance may contain several linkage stages.

The relevant evidence is therefore not only:

`Final Dataset`

but also:

`Source Data + Linkage History + Linkage Quality`

The structure through which evidence was assembled matters to interpretation.

## 10. Longitudinal Analysis Requires Persistent Entity Identity

A longitudinal question asks whether the same entity changed over time.

For example:

`Firm in 2020`

`→ Firm in 2021`

`→ Firm in 2022`

`→ Firm in 2023`

A date field alone is not sufficient.

Researchers also need an entity identity that can be connected across those dates.

The Census Bureau's Longitudinal Business Database is constructed by linking annual business records to create longitudinal histories of establishments and firms.[8]

The current LBD covers U.S. employer businesses over a long historical period and provides measures at establishment and firm level.[8]

The structural requirement is:

`Entity Identity + Time → Longitudinal Evidence`

Repeated cross-sectional observations do not automatically become a longitudinal record merely because they occur in successive years.

## 11. Identifier Change Can Create Apparent Change

An identifier can change even when the underlying economic relationship continues.

Census LEHD documentation provides a direct example.

Its state employer identifier, SEIN, can change because of:

- Change in legal form.
- Merger.
- Divestiture.
- Other administrative events.[9]

LEHD notes that if an employer changes SEIN without an equivalent economic change, workers can appear to have separated from the old employer even though their employment continues.[9]

This can create spurious employer changes and bias employment and job-flow statistics.[9]

The evidence chain can become:

`Administrative Identifier Change`

`→ Apparent Employer Change`

`→ Apparent Worker Separation`

without:

`Equivalent Economic Separation`

Identifier stability therefore affects the relationships visible in longitudinal evidence.

## 12. A Relationship Can Be an Evidence Object of Its Own

Some systems cannot represent important relationships safely inside either entity table.

Consider workers and employers.

One worker may have several employers.

One employer may have many workers.

The relationship is many-to-many.

A separate record can therefore represent the job itself:

`WorkerID | EmployerID | Start | End | Earnings`

The job becomes an evidence object.

Census LEHD explicitly describes job-level data as providing earnings for jobs, where a job is a link between a worker and a firm.[5]

Its files preserve different keys for workers, employers, and establishments, allowing characteristics from these levels to be connected to jobs.[5]

This demonstrates an important principle:

**Sometimes the relationship, rather than either entity alone, is the required unit of analysis.**

## 13. The Relationship Can Be More Important Than Either Entity Table

Suppose researchers possess:

`Worker Characteristics`

and:

`Firm Characteristics`

The analytical question may concern:

`Worker × Firm`

Examples include:

- Worker mobility.
- Earnings by employer characteristics.
- Job duration.
- Movement between firms.
- Skill and industry matching.
- Worker location relative to employer location.

The worker dataset alone cannot reveal these relationships.

The employer dataset alone cannot reveal them.

A structure connecting workers to jobs and jobs to employers can.

Dataset architecture therefore determines whether some relationships exist as observable evidence at all.

## 14. Time Indexing Determines Which Observations Can Be Related

Two records may describe the same entity but different times.

Suppose:

`Firm Revenue: 2024`

and:

`Firm Employment: 2026`

A shared Firm ID establishes entity identity.

It does not make the two observations simultaneous.

SDMX formally includes time as a dimension within statistical data structures.[4]

For many longitudinal relationships, the relevant key is therefore closer to:

`Entity ID + Time`

than:

`Entity ID`

alone.

Without time indexing, researchers may know which entity a value belongs to but not which temporal state it describes.

## 15. Time Structure Determines Which Relationship Is Being Tested

Consider the question:

**Does investment relate to productivity?**

Several structural relationships are possible:

`Investment at Time t ↔ Productivity at Time t`

`Investment at Time t ↔ Productivity at Time t+1`

`Average Investment over Five Years ↔ Productivity at End of Period`

These are different analytical relationships.

A dataset that preserves only broad annual or multi-year aggregates may be unable to distinguish them.

Time structure determines not only whether observations can be connected.

It also determines which temporal relationship the data can represent.

## 16. Time Aggregation Can Remove Sequence Relationships

Suppose a source system collects monthly observations but publishes only annual totals.

Researchers may still examine:

`Annual Revenue ↔ Annual Employment`

They may no longer be able to examine:

`Employment Change Immediately Following a Revenue Shock`

The relevant variables remain present.

The sequence information required by the second question does not.

This illustrates the relationship between dataset structure and evidence resolution.

Aggregation can preserve quantities while removing the indexing structure required to connect events in sequence.

## 17. Geography Can Function as a Linking Dimension

Spatial relationships require compatible geographic structures.

Suppose:

`Dataset A: Hospital Admissions by District`

and:

`Dataset B: Air Pollution by District`

If the same district definitions, identifiers, and effective boundaries apply, a district-level relationship may be observable.

Now suppose Dataset B reports:

`Air Pollution by Postal Zone`

Both datasets contain geographic information.

They do not automatically contain the same geographic unit.

Connecting them may require:

- A common geography.
- A crosswalk.
- Spatial transformation.
- Another defensible mapping.

Geographic information is therefore useful for linkage only when the spatial units themselves are sufficiently compatible.

## 18. The Same Place Name Does Not Guarantee the Same Geographic Entity

Two records can both contain a familiar place name while representing different spatial units.

For example:

`Bangkok`

could refer to different administrative or statistical concepts depending on the dataset.

Geographic boundaries can also change over time while labels remain similar.

A strong geographic relationship may therefore require more than a name.

Relevant information can include:

`Geographic Identifier`

`Boundary Definition`

`Effective Period`

The visible label alone does not establish that two spatial observations cover the same area.

## 19. Hierarchies Determine Which Levels Can Be Connected

Many evidence systems contain hierarchies.

Examples include:

`Person → Household`

`Worker → Job → Establishment → Firm`

`School → District → Region`

`Facility → Company → Corporate Group`

`Sensor → Site → Network`

Census LEHD explicitly distinguishes job, employer, establishment, and national firm information and provides different linkage keys across those structures.[5]

If those relationships are preserved, researchers can move between analytical levels.

If only a firm-level aggregate remains, establishment-level variation may no longer be observable.

Hierarchy is therefore part of the evidence structure.

## 20. Parent-Child Relationships Are Evidence

Knowing that:

`Establishment E exists`

and:

`Firm F exists`

does not establish:

`Establishment E belongs to Firm F`

That relationship requires evidence.

The same principle applies to:

`Person → Household`

`Facility → Company`

`School → District`

The existence of both entities is different from evidence connecting them.

This gives another distinction:

`Available Entities ≠ Available Relationship`

Dataset structure must preserve the parent-child connection if analysis depends on it.

## 21. Aggregation Can Remove Individual-Level Linkability

Suppose:

`Dataset A: Person-Level Health Outcomes`

and:

`Dataset B: Average Income by District`

A researcher may attach the district's average income to a person's health record based on residence.

The resulting analytical relationship is:

`Individual Health ↔ Area-Level Income`

It is not:

`Individual Health ↔ Individual Income`

The concepts of health and income are both present.

The structural level differs.

A dataset can therefore contain information relevant to both sides of a question while lacking the unit-level relationship the claim requires.

## 22. Group-Level Relationships Should Remain Group-Level Claims

Suppose regions with higher average income have lower average disease incidence.

That supports evidence about:

`Region ↔ Region`

It does not independently establish:

`Higher-Income Person ↔ Lower Individual Disease Risk`

The regional evidence may be completely valid.

The issue is the level of inference.

Dataset structure determines the population and unit over which the observed relationship exists.

A relationship should therefore not silently move from one analytical level to another.

## 23. Different Aggregation Levels Can Make Direct Joins Invalid

Consider:

`Dataset A: Revenue by Company`

and:

`Dataset B: Employment by Establishment`

One company may contain several establishments.

A direct join can duplicate company revenue across multiple establishment records.

That can generate mathematically valid rows while overstating or distorting the analytical relationship.

One possible solution is to aggregate establishment employment to company level first.

Another may be to analyze the relationship at establishment level if company revenue can legitimately be allocated.

The correct approach depends on the hierarchy.

Without structural information, software can produce a successful merge that is evidentially wrong.

## 24. A Successful Database Join Is Not Necessarily a Valid Evidence Join

Software can join tables whenever fields contain matching values.

But matching values do not establish semantic equivalence.

Suppose:

`RegionCode = 10`

appears in two datasets.

If each dataset uses a different geographic classification, the technical join may succeed while connecting different places.

Likewise:

`CustomerID = 123`

may uniquely identify a customer only within one year.

The same value appearing the next year may not represent a persistent identity unless the identifier specification establishes that continuity.

Technical joinability and evidentiary compatibility are therefore different properties.

## 25. Uniqueness and Analytical Identity Are Different

A key can be unique and still represent the wrong entity for a particular research question.

Suppose each customer account has a unique:

`AccountID`

If one person can close an account and open another, the identifier reliably distinguishes accounts.

It may not preserve customer identity across account changes.

For:

`Account-Level Analysis`

the key may be appropriate.

For:

`Customer Lifetime Analysis`

it may be insufficient.

This creates another distinction:

`Unique Identifier ≠ Persistent Identifier for Every Analytical Entity`

The key must correspond to the unit required by the claim.

## 26. One Evidence System May Need Several Identifiers

Complex datasets often need separate identifiers for separate entities.

Census LEHD illustrates this directly.

Its infrastructure uses distinct identifiers for:

- Persons.
- Employers.
- Establishments.
- Jobs or job spells.
- National firms.[5]

These identifiers answer different identity questions.

A worker identifier cannot substitute for an employer identifier.

An employer identifier cannot substitute for an establishment identifier.

The structural relationships among them allow different levels of evidence to be connected.

This is why dataset structure is not merely a formatting choice.

It determines the analytical graph available to researchers.

## 27. Structure Determines Which Relationships Survive Reuse

A dataset may be preserved for years while some structural documentation disappears.

The values survive.

The column names survive.

But researchers may no longer know:

- What each record represents.
- Whether identifiers are persistent.
- Which fields form the true key.
- Whether two identifiers refer to the same analytical entity.
- How tables relate.
- Whether geography changed.
- Which time period each record represents.
- Whether linkage was direct or probabilistic.

The dataset remains readable.

Its relationships may no longer be reconstructable with confidence.

Structural documentation is therefore also part of provenance.

## 28. Derived Linked Datasets Have Their Own Evidence State

Suppose:

`Dataset A`

and:

`Dataset B`

are combined using probabilistic record linkage.

The result is:

`Linked Dataset AB`

AB is not merely A plus B.

It contains an additional evidentiary component:

`The asserted relationship between records`

That relationship may have:

- Linking criteria.
- Match probabilities.
- False-positive risk.
- False-negative risk.
- Unmatched records.
- Clerical decisions.
- Quality metrics.

A linked dataset is therefore a derived evidence object.

Its analytical meaning depends partly on how the connection was created.

## Why It Matters

Researchers often begin with a deceptively simple question:

**Do the datasets contain the variables I need?**

That is necessary.

It is not sufficient.

A stronger question is:

**Does the data structure preserve the relationship needed to connect those variables at the unit, time, geography, and level required by the claim?**

A dataset can contain extensive information while lacking the structure required to connect it.

A person table may not connect to jobs.

A job table may not connect to establishments.

A company record may not preserve the same corporate identity through restructuring.

A geographic label may not preserve common boundaries.

A yearly identifier may not support longitudinal tracking.

A group-level statistic may not support an individual-level claim.

The central principle is:

**Dataset structure determines which relationships can become observable evidence.**

Values alone do not create relationships.

The connection between values must also exist in the evidence.

`Available Data ≠ Observable Relationship`

and:

`Relevant Variables ≠ Linkable Records`

## Limits and Uncertainty

This article does not argue that every analytical dataset requires a single universal identifier.

Different research systems legitimately use different structural designs.

Some relationships can be represented through direct identifiers.

Others can be established through:

- Composite keys.
- Foreign keys.
- Crosswalks.
- Deterministic matching.
- Probabilistic linkage.
- Hierarchical mappings.
- Geographic transformation.
- Aggregate alignment.

Nor does the absence of person-level or entity-level linkage make a dataset analytically useless.

Many valid research questions operate at:

- Regional level.
- Sector level.
- Institutional level.
- Population-group level.
- Time-period level.
- Other aggregate levels.

The public sources reviewed for this article do not establish:

- That a unique key is always correct.
- That identifiers are always persistent through time.
- That probabilistic linkage is inherently unreliable.
- That every dataset should be normalized into multiple relational tables.
- That individual-level linkage is required for every research question.
- That technical joinability establishes semantic compatibility.
- That a common column name establishes a common analytical entity.
- That a successful linkage eliminates measurement or comparability problems.
- That more linkage always produces stronger evidence.

The broader principle is narrower:

**The relationship required by a claim must exist, or be defensibly constructed, at the level where that claim is made.**

A dataset does not only determine what information is stored.

Its keys, dimensions, units, hierarchies, identifiers, and relationships determine what researchers can connect.

And what can be connected helps determine what relationships the evidence can reveal.

## Sources

**[1] World Wide Web Consortium.** *Model for Tabular Data and Metadata on the Web.* W3C Recommendation, 17 December 2015. Defines rows as structured information about things and specifies primary keys, including keys composed of multiple cells.

**URL:** https://www.w3.org/TR/tabular-data-model/

**Accessed:** 3 October 2026.

**[2] World Wide Web Consortium.** *Metadata Vocabulary for Tabular Data.* W3C Recommendation, 17 December 2015. Defines primary-key and foreign-key metadata and specifies how referencing values connect to unique rows in tabular data.

**URL:** https://www.w3.org/TR/tabular-metadata/

**Accessed:** 3 October 2026.

**[3] World Wide Web Consortium.** *The RDF Data Cube Vocabulary.* W3C Recommendation. Defines statistical observations through dimensions, measures, and attributes. Dimension values identify observations, measures represent observed phenomena, and attributes provide additional interpretive information.

**URL:** https://www.w3.org/TR/vocab-data-cube/

**Accessed:** 3 October 2026.

**[4] Statistical Data and Metadata eXchange.** *SDMX Information Model* and *SDMX Glossary.* Official SDMX documentation. Defines Data Structure Definitions containing dimensions, measures, and attributes and explains how dimension values and time identify statistical observations.

**URL:** https://docs.sdmx.org/en/i1-doc/Sections/Section2/SDMX_2_1_SECTION_2_InformationModel.html

**URL:** https://sdmx.org/wp-content/uploads/SDMX_Glossary_Version_2_1_December_2020.htm

**Accessed:** 3 October 2026.

**[5] U.S. Census Bureau, Longitudinal Employer-Household Dynamics.** *LEHD Snapshot Documentation.* Official documentation describing job-level and employer-level files, jobs as links between workers and firms, and identifiers used to connect worker, employer, establishment, and national-firm information.

**URL:** https://lehd.ces.census.gov/data/lehd-snapshot-doc/latest/sections/introduction.html

**Accessed:** 3 October 2026.

**[6] U.S. Census Bureau.** "Data Ingest and Linkage." Official administrative-data documentation. Describes probabilistic linkage using identifying information and assignment of Protected Identification Keys for linkage with other Census-held datasets.

**URL:** https://www.census.gov/about/adrm/linkage/technical-documentation/processing-de-identification.html

**Accessed:** 3 October 2026.

**[7] Office for National Statistics.** "Data linkage and matching policy." Official ONS policy defining false-positive and false-negative linkage errors and stating that match rate alone does not measure linkage quality. Recommends evaluation using precision and recall.

**URL:** https://www.ons.gov.uk/aboutus/transparencyandgovernance/datastrategy/datapolicies/datalinkageandmatchingpolicy

**Accessed:** 3 October 2026.

**[8] U.S. Census Bureau.** "Longitudinal Business Database." Official restricted-use data documentation. Describes the LBD as a longitudinal database of U.S. establishments and firms and explains its use for studying business formation, growth, employment dynamics, productivity, and related questions.

**URL:** https://www.census.gov/programs-surveys/ces/data/restricted-use-data/longitudinal-business-database.html

**Accessed:** 3 October 2026.

**[9] U.S. Census Bureau, Longitudinal Employer-Household Dynamics.** "Successor-Predecessor File." Official LEHD documentation. Explains that state employer identifiers can change because of legal-form changes, mergers, divestitures, and other events and that such identifier changes can create spurious employer separations and bias employment and job-flow statistics.

**URL:** https://lehd.ces.census.gov/data/lehd-snapshot-doc/latest/sections/employer_level/spf.html

**Accessed:** 3 October 2026.

---

**Groundline Research Lab**  
**Data • Evidence • Provenance • Research Systems**  
Under the DGCP™ framework

**Commit:** `Add article on dataset structure and observable relationships`
